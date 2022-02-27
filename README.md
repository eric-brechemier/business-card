# business-card
My new business card (2022)

## Rationale

I have been using the same business card design from 2007 to 2021.
I had voluntarily left out my phone number and postal address,
to make the cards timeless. Still, fourteen years is a long time,
and everything that appears on the card apart from my name has
now become outdated:

* after 15 years of work in "Software Design and Development",
  I have been transitioning to Instructional Design.

* the card featured my name and occupation in English and in Japanese,
  and was illustrated with the drawing of a Japanese rock garden,
  in tribute to ten trips to Japan across several years of fruitful
  collaboration with Japanese companies.
  But I have not returned to Japan in the last 12 years.

* it was a stock design and I now need a custom design
  to showcase my graphic design skills.

* I have grown tired of the custom email address used on my business cards,
  and I would rather use a new one which reflects my new occupation.

* the card includes my Skype id, but I have stopped using Skype
  after [Skype dumped me][].

* my website address starts with `http` while today's Web requires `https`;
  I have not updated my personal website in a long time, and I am now relying
  mostly on my LinkedIn profile instead.

[Skype dumped me]: https://github.com/eric-brechemier/how-i-replaced-skype-with-twilio/issues/1

## Design

The front of the card features a fractal shape called [Sierpiński Sieve][]
or [Sierpiński triangle][]. It can be drawn in many different ways;
here I chose to subdivide each triangle by joining the middle of each side.

The back of the card reveals the continuation of the fractal shape,
with lines of text for my details nested in negative space in the
middle of the fractal. But only half of the fractal shape is visible
on that side of the card, because in its growth, it has already
expanded to twice the length of the card. This particular cropping,
which leaves symmetrical shapes missing on the top and bottom of the card,
adds a layer to the visual puzzle started on the front of the card.

[Sierpiński Sieve]: http://mathworld.wolfram.com/SierpinskiSieve.html
[Sierpiński triangle]: https://en.wikipedia.org/wiki/Sierpi%C5%84ski_triangle

## Dimensions

After reviewing the [various sizes][] of business cards commonly found in
different countries, I chose the [credit card size][] for the convenience
of storage in a credit card holder:

|            | inches |    mm |
| ---------: |   ---: | ----: |
| **width**  |    3 ⅜ | 85.60 |
| **height** |    2 ⅛ | 53.98 |

which corresponds to the following ratio:

|            |         `inches x 8` |  `=`  | ratio |
| ---------: | -------------------: | :---: | ----: |
| **width**  | `(3 ⅜) x 8 = 24 + 3` |  `=`  |    27 |
| **height** | `(2 ⅛) x 8 = 16 + 1` |  `=`  |    17 |

which I multiplied by `400` to get dimensions of the view box
in abstract SVG units which preserve the credit card ratio:

|            |`ratio x 400` |  `=`  | SVG units |
| ---------: | -----------: | :---: | --------: |
| **width**  |   `27 x 400` |  `=`  |     10800 |
| **height** |   `17 x 400` |  `=`  |      6800 |

The factor `x400` was chosen to still have dimensions
expressed in round numbers after successive subdivisions:

| subdivision | factor |
| ----------: | -----: |
|         `1` | `x400` |
|       `1/2` | `x200` |
|       `1/4` | `x100` |
|       `1/8` |  `x50` |
|      `1/16` |  `x25` |

[various sizes]: https://en.wikipedia.org/wiki/Business_card#Dimensions
[credit card size]: https://en.wikipedia.org/wiki/Credit_card#Technical_specifications

## Bleed and Safe Area

To account for inaccuracies during trimming of the business card to the
target dimensions after printing, the design must be printed at a slightly
larger, including a bleed area of a few millimeters in width. While visuals
must be printed all the way into the bleed area, important information such
as text must keep safe of the trim boundaries, a few millimeters away from
the trim line on each side. The table below lists a few recommendations for
the width of the bleed area outside the document and the safe margin within:

| bleed | margin | source |
| ----: | -----: | :----- |
| `2mm` | `3mm`  | [Exaprint](https://blog.exaprint.fr/cadres-impression-contraintes-et-astuces/) |
| `⅛in`  | `⅛in` | [Impactica](https://impactica.zendesk.com/hc/en-us/articles/360020899794--What-are-bleed-trim-and-safe-area-) |
| `5mm` | `5mm`  | [Copytop](https://www.copytop.com/astuce-fichiers-pour-une-impression-parfaite) |

Given that:

* `⅛in` is slightly larger than 3mm.
* Exaprint is giving *minimum* indications, but recommends to go with
  more than 2mm of bleed and 5mm of margin for visual comfort.
* Copytop, on the other hand, gives values safe for most usage.

I am going with the largest values of 5mm of bleed and 5mm of safe margin.
Based on Exaprint's recommendations, I should also avoid putting the vertices
of the triangles on the trim lines, to avoid visible inaccuracies. I will not
heed that advice, which should not impact this design, as the shape of
triangles will be completed mentally by the viewer even if one vertex is
cut off, as shown in the Gestalt principle of closure.

## License

[CC-BY][] [Eric Bréchemier][ATTRIBUTION]

[CC-BY]: https://creativecommons.org/licenses/by/4.0/
[ATTRIBUTION]: https://github.com/eric-brechemier/business-card
