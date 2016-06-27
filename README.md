## node-canvas

[node-canvas](https://github.com/Automattic/node-canvas)

Node canvas is a Cairo backed Canvas implementation for NodeJS.

## node-canvas Docker Images

node-canvas docker image

### Usage

Example:

    $ cat index.js                                                                                                                                                      22:12:46
    var Canvas = require('canvas')
      , Image = Canvas.Image
      , canvas = new Canvas(200, 200)
      , ctx = canvas.getContext('2d');
    ctx.font = '30px Impact';
    ctx.rotate(.1);
    ctx.fillText("Awesome!", 50, 100);
    var te = ctx.measureText('Awesome!');
        ctx.strokeStyle = 'rgba(0,0,0,0.5)';
        ctx.beginPath();
        ctx.lineTo(50, 102);
        ctx.lineTo(50 + te.width, 102);
        ctx.stroke();
    console.log('<img src="' + canvas.toDataURL() + '" />');

    $ docker run --rm -v `pwd`:/opt/node/js geekduck/nodecanvas index.js
        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMgAAADICAYAAACtWK6eAAAABmJLR0QA/wD/AP+gvaeTAAAMFElEQVR4nO3dd7AdZRmA8SckJJSEQDRAQpAIigg2RCni0ARslEHB3lBhwIIKIg5WcEYBxQoKKhoENYiKymBBBTvgWEC6YigqJLQgKcaQXPzj3XXfs3d370m9N8nzm9k5e/Z7t5yT/far5wYkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZIkSZK0hhk93BewEp0M7AJsAwwA9w/v5UgjxwuBR9NyzfBejjSy/IbeDLIEmDSsVySNEM+nN3OUy0uG86KkkeJ3VJni4bT+heG8KGkkOJAqQ/wXeEN6/9fhuyxpZPgVVYY4CxgLzE/bHj98lyYNrwOoMsIiYOti+4/S9jd37L8bsDswDVh/1V2mNDxyz9Xn0/YT0vaZHfufm+Le1RIzATgE2BXYbAWvV1ptnkdv2+NxKe3pKe0+YL2WY7wzxX2xJeYoeqtwTcYARwMHA88q3kvD6pc0lx4Ao4B7UvrOLcfI3cO/bom5KsVc0RJzcIr5F2vX7AStgfajvfQofT3FvKflOFunmAca0nco0hYWr3NajvPtdJzThrj2vYCvAbcBS4EFwN+Bi4lxm7bSTupb7rk6pyXmyBRzeUvMKHrHTbaopZ+ezvFQsT65FvNYIpOWx9ih5VwbERmjaUAzL1fRnOGzqUS76CjgdcDewCZD7KN1xL70lh7btMTl0mEhsEFL3DUpbt+0fQxwd7F9V6rByH1q+x+X9v9dyznGAj9l6MxRLrOIjFc3mShpljbsMwDcBLwb2LTlOrQO+AXVTbGAaDtcBHyaqEq9lmjA70jcaGXs/i3Hm5Fi3pK2H1Rsu6F4/+WGGIA/pf2PbjnHe1PMXKJz4AlEr9gEoqv5NKKruow7r3aMUfTOGOharm+5jmwq8Fbgc0Rv3qeJEmldGjd6M/GZDwLGD/O1rBT70P9TuL60tQ1OSjG5l+o7xbYTivfHF+/PTjG5t2whMLHh+BtSVc8eBrbv+Hx7AIuL2P/QWxI8p/Z57gN+CHyLeGjMS2m/7DjHhsBngUdo/p6WApcC0zuO8RiiCvsi4MkdcSPdnVSfe614MFzJ8meQP7QcM/dAlb1Uk4nq22KqdskLipgr076fSvte2HL8w1PMdVQl3E40zzaekeJzqfemtP1aBrc5RhNdzOcDF7Rcyzjg5/T3fT0IPKPlOM9NcVcV2zYDjiXaWd8kHjxPaNl/JFiPqu04QHsVfI3ps9+bqv6/GHgm8cG2ALYqXqel182L17Lo3Jmo19d/RHVzWi+fhq8m2g3fp+q5uql43al4HVvElWa0XPez0/rTiBsoWwTMJto7s4FtU9rWaX12Wv8bURplS4mHwOuLa2tyCtEDWLqV6O2bQ5RWBxKZF+KGv5T4TubXjjM1rd9d7HMhsGXa/grgQ8DbgK+k7VsBLy+OOx64hchQq3ve3GOpvqe5xL/DGu0KqqfWucuwX663v6whfTRRnSljJhFP+keBQ1Nc7vGaDByW9rmD9u7Z79LfE7tpeW06zvrAX1LapcRUm37HXLagt41zPs0Z6SX09sq9ryHmHSn9t/TOfasvi6keEm9siV1SHHN1ytXjftpsI9peVB/mv3TXj+tOTfu2jZZfm2LKXqnZDJ6fVfZ47UOULuU+p3acP88Lm0lUf64kSq7cbmhaXlQ71iTiaZtjZhNtp6d0XANEg7zc5+aGz5a9P8Xe2JB+Or3XMA/4MFHK7w98jN7MeCFRsnV91gF6S7c26xPV1ouKz3EHUfpcBpxIbynWJf8CtW0YYI2R681tN3mbnLlmtcTkm+7e4vUTDXFfLdJOoWpMDwDbdZx/Zjr2oQ3pGwNPKq7zVcScsE8SVZ+2Bv0OwEeJAcZ8k/0MeGIf13Fcx/VCVD/KruSlDK6f5/Gc+TS3VV6RYhYQpfRDRObbi6jOnVaklXE/GeK6nkxvr2HTMp+o1g3ljWmfGX3Ej1gTiS7ImcQA4fRl3H8svU/qppv5Awz+ondqiDuxSMuDi78Y4vwnp9i2xvOK2KM47kBxjvtp/oy5lHx2Q3rdP1P89Fraz1Ja04MEom07N8XNpbnHK5cs/6G9ZNuR6uHVz3JS98frKSU/NkTsWu8yqi/jmIb03NP0KO1/8OEgBv9DvGGIc29HdfMu7SMelq/3J1ehzm9IvyOlb92QXndXip9WS7sxpT2/4xh5HOrDLTEbUk3leZRoxNeNAf6cYq4jxjCeRHRqPJ0Yz7g+xTwCPLXj2s5OsW/viBvxdicaiscRxeIRRJfrnsQXsy3RaG7ruYH40g8gpmUc2JC+I703fVMmojhXve7dzwDTl2r7fZ/oMMhTSiYRXc4XEVWnbBpwBt09jvnabmlIvyOlt02HKY2jGidZQtzEWS4ZNu84Th5n2LMjLpcM0xvSX5nSf9pwPaUxxEyDMrZtGhLAJSnu8I64Ed/NezXRfTmhWMan9c3T+4lET9I8oh46Ly3ziZvuWuDfDee4qTjWFkQX5lUNMRA32UJiXhXEP0a9C7TJ8cTTbLfi/SHFQnF9A/QOMtbPP5Wo3u1HjML/puEch6X1gYb0O6mm5exBcyYq7U91X9xGVH1KG1INYD5C+98eG0Xv3LY/d5wv98TNa0h/TVq/mvjbZ2XX+MKUtoR4uB1WHDNPHarLU3n+2RE34jMIxAefWyxdxrDiGek2olG6iLgBsgHiqT+FqKbcRH/mESXYZ4gq1qiUNqHhHPVp9VOK112IqTU3EKPl/yg+825E9a/0+4Zr+DXROIaYrzWT3hu/tD7wwfT+x7X0PAZyD82ZEWK0fVyx/hC9N3I2juqHaIuJAcq63dP6+4ul9DDxE4M56XUxkZG7Jn1unNZv7Yjr+cdaV9Qz0mbpfbltE6pq1FyaM9M8okRqu0maPJWo6u1DVO02Im6em4ku4QsYPGg2npgecmQfx19AZJh69+z2xbbygXgFUWW9M8VMIqqD5Z9LGiAGWP+SYp5L9duZa+i9ebOnEW0FiAdJU6cHRJXq9mL9LgZPPp1MVMGWx0J6M0J2C9GGuZfBs7h7rAklyMrWb4m0AYMzzmbEk6l8P5F4YtUzTltGup6oLi2L+cTNPJPoGm37AdgsooRqGrv4K3AmVe/OfkS18xriybsJcfPnG+ocejMHDB5Fb1MvafqJazreRmn9QWIMaUuiXTmFqpRq0vXvW37OrqomsG5mkH4tKpb7hohbFRmpyeXFsgtRXZpanHsOcaNfQfSUtTmZqPqUf8hiNDEJssllNP9Of0pa78og/cYNlZEWpPWFDG5QP6Y411ZUGWdLomOjK4OUGa+zegVmkJVhdWekWUSjd1mqdhTxRxHTVE4kepbqVex/EGMbZ7Ucf3lKkBXJSPcTDfLypt+Z3gb/A8Vyw+BdO51eHO/nQwWaQVafkVIi/aBYJhOj4JsSJc8sogrYVQotT8mwolWxi6nGKs4jetmaGvPZ5nS3Xc4YYv//M4OMPKszI93KsnU2XE5Ue7aidyZ0Xc5I/bZB2uLOJNpWE4gS5Drg48SYyK1U1z2R6M07hujw+GjHeftmBllzDUeJ9A3af/uSXVZc1xS66/n9lEh3Eu2mrxP36zSiyxwiYz9ANNbzKHyeYl/3GmLO2hwiI93eEbtOdvOqWVNGqr/vNyOVv6IcyrHEb3u2JAZU/9YR+2JisurUjhiIxvx+tE8Z+h7VxNGXEj9JaGUG0bLqJyNtSvw0YWVlpNIEYhzpCCJjlQOti4nG+yVEO6Xrfxf7PdWEzT2I0flWZhCtKqs6I40q9t+AqM4t6fO6/kVVCm1DDFC2sg2iVWVF2kiTiQmY5baNiYw0l+bMRPG+/MVil48QGWQavT9lbmQJojXBaGJwr6kUyu/LeXRNpVB+309GAswgWruMpppLt3HxOj69lplqHJFJHqbKQPcCf6wf0CqW1iZLia7fpp81ZDkjlRlnWToLJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJEmSJElad/0PNzwq+B0sZB8AAAAASUVORK5CYII=" />