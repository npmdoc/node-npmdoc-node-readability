# api documentation for  [node-readability (v2.2.0)](https://github.com/luin/node-readability)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-readability.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-readability) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-readability.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-readability)
#### Turning any web page into a clean view.

[![NPM](https://nodei.co/npm/node-readability.png?downloads=true)](https://www.npmjs.com/package/node-readability)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-readability/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-readability_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-readability/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-readability/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-readability/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Zihua Li"
    },
    "bin": {
        "readability": "./src/cli.js"
    },
    "bugs": {
        "url": "https://github.com/luin/node-readability/issues"
    },
    "config": {
        "commitizen": {
            "path": "./node_modules/cz-conventional-changelog"
        }
    },
    "dependencies": {
        "encoding": "~0.1.7",
        "jsdom": "^6.3.0",
        "minimist": "^1.2.0",
        "request": "~2.40.0"
    },
    "description": "Turning any web page into a clean view.",
    "devDependencies": {
        "cz-conventional-changelog": "^1.1.5",
        "mocha": "~1.8.2",
        "nock": "~0.27.1",
        "should": "~2.1.1"
    },
    "directories": {},
    "dist": {
        "shasum": "341606508ad80b14aac498feba9e8194d86778e7",
        "tarball": "https://registry.npmjs.org/node-readability/-/node-readability-2.2.0.tgz"
    },
    "engines": {
        "node": ">= 2"
    },
    "gitHead": "206b37021ceed0f029174bd3dd716e1677224ffa",
    "homepage": "https://github.com/luin/node-readability",
    "keywords": [
        "readability"
    ],
    "licenses": [
        {
            "type": "Apache License 2.0",
            "url": "http://www.apache.org/licenses/LICENSE-2.0"
        }
    ],
    "main": "./src/readability",
    "maintainers": [
        {
            "name": "luin",
            "email": "i@zihua.li"
        }
    ],
    "name": "node-readability",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/luin/node-readability.git"
    },
    "scripts": {
        "test": "mocha -R spec"
    },
    "version": "2.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-readability](#apidoc.module.node-readability)
1.  [function <span class="apidocSignatureSpan">node-readability.</span>read ()](#apidoc.element.node-readability.read)
1.  object <span class="apidocSignatureSpan">node-readability.</span>helpers

#### [module node-readability.helpers](#apidoc.module.node-readability.helpers)
1.  [function <span class="apidocSignatureSpan">node-readability.helpers.</span>debug (debug)](#apidoc.element.node-readability.helpers.debug)
1.  [function <span class="apidocSignatureSpan">node-readability.helpers.</span>getInnerText (e, normalizeSpaces)](#apidoc.element.node-readability.helpers.getInnerText)
1.  [function <span class="apidocSignatureSpan">node-readability.helpers.</span>grabArticle (document, preserveUnlikelyCandidates)](#apidoc.element.node-readability.helpers.grabArticle)
1.  [function <span class="apidocSignatureSpan">node-readability.helpers.</span>prepDocument (document)](#apidoc.element.node-readability.helpers.prepDocument)
1.  [function <span class="apidocSignatureSpan">node-readability.helpers.</span>setCleanRules (rules)](#apidoc.element.node-readability.helpers.setCleanRules)



# <a name="apidoc.module.node-readability"></a>[module node-readability](#apidoc.module.node-readability)

#### <a name="apidoc.element.node-readability.read"></a>[function <span class="apidocSignatureSpan">node-readability.</span>read ()](#apidoc.element.node-readability.read)
- description and source-code
```javascript
read = function () {
  console.warn(''readability.read' is deprecated. Just use 'var read = require("node-readability"); read(url...);'.');
  return read.apply(this, arguments);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-readability.helpers"></a>[module node-readability.helpers](#apidoc.module.node-readability.helpers)

#### <a name="apidoc.element.node-readability.helpers.debug"></a>[function <span class="apidocSignatureSpan">node-readability.helpers.</span>debug (debug)](#apidoc.element.node-readability.helpers.debug)
- description and source-code
```javascript
debug = function (debug) {
  dbg = (debug) ? console.log : function() {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-readability.helpers.getInnerText"></a>[function <span class="apidocSignatureSpan">node-readability.helpers.</span>getInnerText (e, normalizeSpaces)](#apidoc.element.node-readability.helpers.getInnerText)
- description and source-code
```javascript
getInnerText = function (e, normalizeSpaces) {
  var textContent = "";

  normalizeSpaces = (typeof normalizeSpaces == 'undefined') ? true : normalizeSpaces;

  textContent = e.textContent.trim();

  if (normalizeSpaces) return textContent.replace(regexps.normalizeRe, " ");
  else return textContent;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-readability.helpers.grabArticle"></a>[function <span class="apidocSignatureSpan">node-readability.helpers.</span>grabArticle (document, preserveUnlikelyCandidates)](#apidoc.element.node-readability.helpers.grabArticle)
- description and source-code
```javascript
grabArticle = function (document, preserveUnlikelyCandidates) {
<span class="apidocCodeCommentSpan">  /**
   * First, node prepping. Trash nodes that look cruddy (like ones with the class name "comment", etc), and turn divs
   * into P tags where they have been used inappropriately (as in, where they contain no other block level elements.)
   *
   * Note: Assignment from index for performance. See http://www.peachpit.com/articles/article.aspx?p=31567&seqNum=5
   * TODO: Shouldn't this be a reverse traversal?
   **/
</span>  var nodes = document.getElementsByTagName('*');
  for (var i = 0; i < nodes.length; ++i) {
    var node = nodes[i];
    // Remove unlikely candidates */
    var continueFlag = false;
    if (!preserveUnlikelyCandidates) {
      var unlikelyMatchString = node.className + node.id;
      if (unlikelyMatchString.search(regexps.unlikelyCandidatesRe) !== -1 && unlikelyMatchString.search(regexps.okMaybeItsACandidateRe
) == -1 && node.tagName !== 'HTML' && node.tagName !== "BODY") {
        dbg("Removing unlikely candidate - " + unlikelyMatchString);
        node.parentNode.removeChild(node);
        continueFlag = true;
      }
    }

    // Turn all divs that don't have children block level elements into p's
    if (!continueFlag && node.tagName === 'DIV') {
      if (node.innerHTML.search(regexps.divToPElementsRe) === -1) {
        dbg("Altering div to p");
        var newNode = document.createElement('p');
        newNode.innerHTML = node.innerHTML;
        node.parentNode.replaceChild(newNode, node);
      } else {
        // EXPERIMENTAL
        Array.prototype.slice.call(node.childNodes).forEach(function(childNode) {
          if (childNode.nodeType == 3 /*TEXT_NODE*/ ) {
            // use span instead of p. Need more tests.
            dbg("replacing text node with a span tag with the same content.");
            var span = document.createElement('span');
            span.innerHTML = childNode.nodeValue;
            childNode.parentNode.replaceChild(span, childNode);
          }
        });
      }
    }
  }

  /**
   * Loop through all paragraphs, and assign a score to them based on how content-y they look.
   * Then add their score to their parent node.
   *
   * A score is determined by things like number of commas, class names, etc. Maybe eventually link density.
   **/
  var allParagraphs = document.getElementsByTagName("p");
  var candidates = [];

  for (var i = 0; i < allParagraphs.length; ++i) {
    var paragraph = allParagraphs[i];
    var parentNode = paragraph.parentNode;
    var grandParentNode = parentNode.parentNode;
    var innerText = getInnerText(paragraph);

    // If this paragraph is less than 25 characters, don't even count it.
    if (innerText.length < 25) continue;

    // Initialize readability data for the parent.
    if (typeof parentNode.readability == 'undefined') {
      initializeNode(parentNode);
      candidates.push(parentNode);
    }

    // Initialize readability data for the grandparent.
    if (typeof grandParentNode.readability == 'undefined') {
      initializeNode(grandParentNode);
      candidates.push(grandParentNode);
    }

    var contentScore = 0;

    // Add a point for the paragraph itself as a base. */
    ++contentScore;

    // Add points for any commas within this paragraph */
    contentScore += innerText.replace('，', ',').split(',').length;

    // For every 100 characters in this paragraph, add another point. Up to 3 points. */
    contentScore += Math.min(Math.floor(innerText.length / 100), 3);

    // Add the score to the parent. The grandparent gets half. */
    parentNode.readability.contentScore += contentScore;
    grandParentNode.readability.contentScore += contentScore / 2;
  }


  /**
   * After we've calculated scores, loop through all of the possible candidate nodes we found
   * and find the one with the highest score.
   **/
  var topCandidate = null;
  candidates.forEach(function(candidate) {
    /**
     * Scale the final candidates score based on link density. Good content should have a
     * relatively small link density (5% or less) and be mostly unaffected by this operation. ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-readability.helpers.prepDocument"></a>[function <span class="apidocSignatureSpan">node-readability.helpers.</span>prepDocument (document)](#apidoc.element.node-readability.helpers.prepDocument)
- description and source-code
```javascript
prepDocument = function (document) {
  var frames = document.getElementsByTagName('frame');
  if (frames.length > 0) {
    var bestFrame = null;
    var bestFrameSize = 0;

    Array.prototype.slice.call(frames, 0).forEach(function(frame) {
      var frameSize = frame.offsetWidth + frame.offsetHeight;
      var canAccessFrame = false;
      try {
        frame.contentWindow.document.body;
        canAccessFrame = true;
      } catch (e) {}

      if (canAccessFrame && frameSize > bestFrameSize) {
        bestFrame = frame;
        bestFrameSize = frameSize;
      }
    });

    if (bestFrame) {
      var newBody = document.createElement('body');
      newBody.innerHTML = bestFrame.contentWindow.document.body.innerHTML;
      newBody.style.overflow = 'scroll';
      document.body = newBody;

      var frameset = document.getElementsByTagName('frameset')[0];
      if (frameset) {
        frameset.parentNode.removeChild(frameset);
      }
    }
  }

  // turn all double br's into p's
  // note, this is pretty costly as far as processing goes. Maybe optimize later.
  // document.body.innerHTML = document.body.innerHTML.replace(regexps.replaceBrsRe, '</p><p>').replace(regexps.replaceFontsRe, '<$
1span>');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-readability.helpers.setCleanRules"></a>[function <span class="apidocSignatureSpan">node-readability.helpers.</span>setCleanRules (rules)](#apidoc.element.node-readability.helpers.setCleanRules)
- description and source-code
```javascript
setCleanRules = function (rules) {
  cleanRules = rules;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
