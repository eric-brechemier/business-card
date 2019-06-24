# business-card
My new business card (2019)

## Rationale

I have been using the same business card design from 2007 to 2019.
I had voluntarily left out my phone number and postal address,
to make the cards timeless. Still, twelve years is a long time,
and everything that appears on the card apart from my name has
now become outdated:

* after 15 years of work in "Software Design and Development",
  I am now becoming a graphic designer as well as a programmer

* the card featured my name and occupation in English and in Japanese,
  and was illustrated with the drawing of a Japanese rock garden,
  in tribute to ten trips to Japan across several years of fruitful
  collaboration with Japanese companies.
  But I have not returned to Japan in the last 10 years.

* it was a stock design and I now need a custom design
  to showcase my skills as a graphic designer

* I have grown tired of the custom email address used on my business cards,
  and I would rather use a new one which reflects my new occupation

* the card includes my Skype id, but I have stopped using Skype
  after [Skype dumped me][]

* my website address starts with `http` while today's Web requires `https`

[Skype dumped me]: https://github.com/eric-brechemier/how-i-replaced-skype-with-twilio/issues/1

## Design

The front of the card features a fractal shape called [Sierpiński Sieve][]
or [Sierpiński triangle][]. It can be drawn in many different ways;
here I chose to subdivide each triangle by joining the middle of each side.

The back of the card reveals the continuation of the fractal shape,
with 5 lines of text for my details nested in negative space in the
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

which I multiplied by `200` to get dimensions of the view box
in abstract SVG units which preserve the credit card ratio:

|            |`ratio x 200` |  `=`  | SVG units |
| ---------: | -----------: | :---: | --------: |
| **width**  |   `27 x 200` |  `=`  |      5400 |
| **height** |   `17 x 200` |  `=`  |      3400 |

The factor `x200` was chosen to still have dimensions
expressed in round numbers after successive subdivisions:

| subdivision | factor |
| ----------: | -----: |
|           1 | `x200` |
|           ½ | `x100` | 
|           ¼ |  `x50` |
|           ⅛ |  `x25` |

[various sizes]: https://en.wikipedia.org/wiki/Business_card#Dimensions
[credit card size]: https://en.wikipedia.org/wiki/Credit_card#Technical_specifications

## License

[CC-BY][] [Eric Bréchemier][ATTRIBUTION]

[CC-BY]: https://creativecommons.org/licenses/by/4.0/
[ATTRIBUTION]: https://github.com/eric-brechemier/business-card
