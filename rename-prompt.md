You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "AAT-Employer-Scheme.html",
    "context": {
      "title": "BedfordSquare | Investing In Employees",
      "first_heading": "We areAAT'sFirst Approved Employerin INDIA"
    }
  },
  {
    "path": "April-2020.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "Excerpts from an interview withPRABAHARAN R"
    }
  },
  {
    "path": "Archives.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "BedfordSquare"
    }
  },
  {
    "path": "Articles-and-Features.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "BedfordSquare"
    }
  },
  {
    "path": "August-2020.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "The lockdown has been hard on everyone around the world. At Bedford Square, we have tried to find an opportunity in these difficult times. In view of the COVID situation which led to considerable decr"
    }
  },
  {
    "path": "Event-Gallery.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "Events Gallery"
    }
  },
  {
    "path": "Feb-2020.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "Excerpts from an interview withAMBRASH KANNA RMonth: February 2020"
    }
  },
  {
    "path": "GALLERY.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "BedfordSquare"
    }
  },
  {
    "path": "Jan-2020.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "Excerpts from an interview withARAVINTHMonth: January 2020"
    }
  },
  {
    "path": "July-2020.html",
    "context": {
      "title": "",
      "first_heading": "The \"new normal\" amidst LockdownMasks on, far away from colleagues, closer to home, business as usual..."
    }
  },
  {
    "path": "May-2020.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "Excerpts from an interview withAMBRASH KANNA RMonth: February 2020"
    }
  },
  {
    "path": "PART-III.html",
    "context": {
      "title": "BedfordSquare | Our Story",
      "first_heading": "Our Story - PART IIILight at the beginning of the tunnel"
    }
  },
  {
    "path": "STORY---PART-1.html",
    "context": {
      "title": "",
      "first_heading": "Our StoryThe Journey from the City to the Temple Town"
    }
  },
  {
    "path": "STORY---PART-II.html",
    "context": {
      "title": "BedfordSquare | Our Story",
      "first_heading": "Our Story - PART IIEmpowering our Staff through Education during the Pandemic"
    }
  },
  {
    "path": "Training-Program-at-BSKC.html",
    "context": {
      "title": "BedfordSquare | Investing In Employees",
      "first_heading": "BedfordSquare"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "IntroducingBedfordSquareThe team that keeps your books updated, always."
    }
  },
  {
    "path": "accreditations.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "WE ARE THE FIRST\u200b"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "GET IN TOUCH"
    }
  },
  {
    "path": "css/3bb900a9da1ff294d50fa4009df5a36d.css",
    "context": {
      "path": "css/3bb900a9da1ff294d50fa4009df5a36d.css"
    }
  },
  {
    "path": "css/499b3ed2a6ddcf3ffddcfb451ff19aee.css",
    "context": {
      "path": "css/499b3ed2a6ddcf3ffddcfb451ff19aee.css"
    }
  },
  {
    "path": "css/4ba1f7eeea678c518b19a8a229705620.css",
    "context": {
      "path": "css/4ba1f7eeea678c518b19a8a229705620.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css",
    "context": {
      "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "employees-speak.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "The \"new normal\" amidst LockdownMasks on, far away from colleagues, closer to home, business as usual..."
    }
  },
  {
    "path": "home-backup.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "WE ARE THE FIRST"
    }
  },
  {
    "path": "imgs/013b3ecc3f8682cdc6c017438f3ea198.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/01853ebc20a4e1b434e07569e30dd9c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/074836f3c0fd794000e9f3c1c93d7420.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c1ed0f28b1fd1bab05b75a76773af9a.webp",
    "context": {
      "refs": [
        {
          "alt": "WE work with ACCA",
          "title": ""
        },
        {
          "alt": "WE work with ACCA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0eb09e8770304754cc78684da7e49d14.webp",
    "context": {
      "refs": [
        {
          "alt": "FinalFileLayers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1059b7e6aa5a1a9984b6600902c3a92f.gif",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/16ffb219825fba5360d372c5ffaecc6a.webp",
    "context": {
      "refs": [
        {
          "alt": "LEARNING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/193044e3973b2588e0ccb78abd31043a.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1f34e1f097566b570f7e0380b6b50acc.webp",
    "context": {
      "refs": [
        {
          "alt": "services",
          "title": ""
        },
        {
          "alt": "services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/21965de308815e8ce1ed3362b9809bfa.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c3e9e69f29f15d8d913a20ab8a047a0.webp",
    "context": {
      "refs": [
        {
          "alt": "OTHER SERVICES",
          "title": ""
        },
        {
          "alt": "OTHER SERVICES",
          "title": ""
        },
        {
          "alt": "OTHER SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2dea70dcd0554ebe8bce1b7f76929c42.webp",
    "context": {
      "refs": [
        {
          "alt": "OUR VISION",
          "title": ""
        },
        {
          "alt": "OUR VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fd512aa5b5ecc6a50a2d191a77de3db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/358148169b7edc2d0048548455f2d0fe.webp",
    "context": {
      "refs": [
        {
          "alt": "BALA",
          "title": ""
        },
        {
          "alt": "BALA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37ca9498da9902bc7fc31c52c90891d8.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a8b392072143a3476971e992e173a9e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3eae07e8d853b0ff884e0480156bc039.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/416eb07bd5a69f0291fc8de112ac2893.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42f2d2049e8986d460fa9710f40380e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/44f73d4953fb68b9c8a399b89710de83.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4adf8b036cbf955e889e32c3ffd3aec1.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImageatAM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4f1c9ca41e1b48bd52d672ee0c565148.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5272d11bf797f4170bec4e077c67d439.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5533bd5772c4e50c3241d3a3add352b3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/571629bfb35ff5df607eea144b86b6cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5c3a03704c9622ffc0177ea3c9af27f9.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5c989ae750b04aa8f4dda14091965114.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d9dee389005859062867b2d500d152e.webp",
    "context": {
      "refs": [
        {
          "alt": "FinalFileLayers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e142705d53e0f5de3fdc8ed39aaa1df.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63ab77c27d5d7f2824c5abb7f1be7ee6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67aa8522bc6f6493bcc3f2a6524f732f.webp",
    "context": {
      "refs": [
        {
          "alt": "Company",
          "title": ""
        },
        {
          "alt": "Company",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7066bba8b85480a078b5e8bc8a6e3b21.webp",
    "context": {
      "refs": [
        {
          "alt": "CERTIFICATION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/770e30ccba0ab6a437240c03e7d5e999.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImageatAM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/77adee5e2c6100f475ce5b3b7122a960.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78e649f100a288507fd6f24cff40df34.webp",
    "context": {
      "refs": [
        {
          "alt": "FinalFileLayers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78fe5dc93c9d8aabf7a233f415a6ae66.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86cbe4b3710521c28291798281e37441.webp",
    "context": {
      "refs": [
        {
          "alt": "WE ARE THE FIRST\u200b",
          "title": ""
        },
        {
          "alt": "WE ARE THE FIRST\u200b",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8bef5c233ff8c24816581a06c9d3d282.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8fc3a1ba856c14a6e0a613eb81acf90a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90b5700a613345fce4a85b3b4f9ef345.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91e3e5ac90253109e673406f9d03875e.webp",
    "context": {
      "refs": [
        {
          "alt": "ACCOUNTING SERVICES",
          "title": ""
        },
        {
          "alt": "ACCOUNTING SERVICES",
          "title": ""
        },
        {
          "alt": "ACCOUNTING SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/93d6bd86086235ec4380234aa1895f88.webp",
    "context": {
      "refs": [
        {
          "alt": "Customers",
          "title": ""
        },
        {
          "alt": "Customers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/990edaef3261c6a949ac004cd4807a3d.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c964e92ad4e6e832e0c0d54491bcca8.webp",
    "context": {
      "refs": [
        {
          "alt": "Incentives For Employees",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab602c01e1b82356acf925b0fdb63882.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/adcea2692f362c89543191d01ce6a2a9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af84247f179e6dcfe6ffb35850af1409.webp",
    "context": {
      "refs": [
        {
          "alt": "IceBergUnit",
          "title": ""
        },
        {
          "alt": "IceBergUnit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0a14ac991072e4a7a9f5435691267d7.webp",
    "context": {
      "refs": [
        {
          "alt": "The Proud Finishers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2269ce9d653340f528499786615d39e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b44c4d985e0f31abc828e40cefbf7772.webp",
    "context": {
      "refs": [
        {
          "alt": "FinalFileLayers",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b462ae878d7d5db0408681ba77af6a4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b98049748cf781f5593c0699958a0fc4.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/baa41691e898d7c98e4a7e001b9af3b5.webp",
    "context": {
      "refs": [
        {
          "alt": "SHANTHI B",
          "title": ""
        },
        {
          "alt": "SHANTHI B",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bbc0caa3617ad45c33ba0971e8a7df09.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c11f6488465dded8c6c4cc2b84edc1b3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c3ccd33505e1de25bd4bb295604343c7.webp",
    "context": {
      "refs": [
        {
          "alt": "ALLIED SERVICES",
          "title": ""
        },
        {
          "alt": "ALLIED SERVICES",
          "title": ""
        },
        {
          "alt": "ALLIED SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c3e46df736549e9dc03e00eddd35f678.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c66fcd2a2ee54743fadc9886b91a1f6d.webp",
    "context": {
      "refs": [
        {
          "alt": "aat",
          "title": ""
        },
        {
          "alt": "aat",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd290f445e6c51f6d7716fe5cb335764.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce4749c034948bb43c2cd88aedb8b4e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cea52f3819727907ad5638382bec444a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1a41b073e1d665061fbc128675b2d01.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d4cfaccfd82373246b0b9c984804dc95.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d52a674d0d8e806936a8971d041aef66.webp",
    "context": {
      "refs": [
        {
          "alt": "Employees",
          "title": ""
        },
        {
          "alt": "Employees",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d853228e0a833cc425e4aa8af85ae3a1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da73779ecf2f3318198645343aa39342.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImageatAM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcad3419fe87767a2c56e9890bb242dd.gif",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/df88c0cf4e90d4ebc56056308bdefa1c.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1b72c1f81c32be69df329b83622aff2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e292b503d58efe263f26abd0e43cf3f6.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eed44851630e877c97c39938faf6c123.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eed84fe7b6126cc38de290f4198e6399.webp",
    "context": {
      "refs": [
        {
          "alt": "Journeyfromthecityfinal",
          "title": ""
        },
        {
          "alt": "Journeyfromthecityfinal",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0b4b8ff784a3d6ff77969a2ad097643.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/f5363328f20e3ffe5cb5a2f6cae68525.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f9dc58e68ccc60ff1683f6269ee2d48d.webp",
    "context": {
      "refs": [
        {
          "alt": "HIGHER EDUCATION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fadc81d4d6fc5c6ab61d3ae885062927.gif",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc4b75d6a22860f59ef0cb08500ae2e9.webp",
    "context": {
      "refs": [
        {
          "alt": "The Fit Bytes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd335623ff880031edf22bad4f72136f.webp",
    "context": {
      "refs": [
        {
          "alt": "acca",
          "title": ""
        },
        {
          "alt": "acca",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fdf6cd52ce20f2de96d62843d4646f97.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "WEprovide Accounting and Allied Services to our clients in UK from India\u200bStriving for ZERO DEFECT JOBS\u2026. ALWAYS!\u200b"
    }
  },
  {
    "path": "investing-in-employees.html",
    "context": {
      "title": "BedfordSquare | Investing In Employees",
      "first_heading": "WE HIREB. Com, M. Com, B. Sc. (Math) and M. Sc. (Math) graduatesEligible candidates are expected to be familiar with MS Excel and have typing skills(minimum lower typing of 30 wpm)The Company provides"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "locations.html",
    "context": {
      "title": "BedfordSquare | Locations",
      "first_heading": "Kumbakonam"
    }
  },
  {
    "path": "our-mission-and-core-values.html",
    "context": {
      "title": "BedfordSquare | About Us",
      "first_heading": "OUR MISSION"
    }
  },
  {
    "path": "our-service.html",
    "context": {
      "title": "BedfordSquare | Our Offerings",
      "first_heading": "ACCOUNTINGSERVICES"
    }
  },
  {
    "path": "our-story.html",
    "context": {
      "title": "BedfordSquare | Our Story",
      "first_heading": "Our Story - PART IIEmpowering our Staff through Education during the Pandemic"
    }
  },
  {
    "path": "our-team.html",
    "context": {
      "title": "BedfordSquare | Our Team",
      "first_heading": "SHANTHI B"
    }
  },
  {
    "path": "what-we-do-overview.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "UK Accounting Services from India"
    }
  },
  {
    "path": "what-we-do.html",
    "context": {
      "title": "BedfordSquare | What we do",
      "first_heading": "UK Accounting Services from India"
    }
  },
  {
    "path": "who-we-are.html",
    "context": {
      "title": "BedfordSquare | Who we are",
      "first_heading": "IntroducingBedfordSquareThe team that keeps your books updated, always."
    }
  },
  {
    "path": "women-empowerment.html",
    "context": {
      "title": "BedfordSquare | Home",
      "first_heading": "BedfordSquare"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.