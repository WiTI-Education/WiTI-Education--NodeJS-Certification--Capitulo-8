# WiTI-Education--NodeJS-Certification--Capitulo-8

## Parallel Execution
In the labs-1 folder, theparallel.jsfile containsthe following:
```javascript

const print = (err, contents) => {
    if (err) console.error(err)
    else console.log(contents)}
    const opA = (cb) => {
        setTimeout(() => {
            cb(null, 'A')
            }, 500)}
    const opB = (cb) => {
        setTimeout(() => {
            cb(null, 'B')
            }, 250)}
    const opC = (cb) => {
        setTimeout(() => {
            cb(null, 'C')
            }, 125)}

```
The opA function must be called before opB, and opB must be called before opC.Call functions inparallel.jsin such a way that C then B then A is printed out.

## Serial Execution

In the labs-2 folder, theserial.jsfile containsthe following:

```javascript
const { promisify } = require('util')
const print = (err, contents) => {
    if (err) console.error(err)
    else console.log(contents)}
    const opA = (cb) => {
        setTimeout(() => {
            cb(null, 'A')
            }, 500)}
    const opB = (cb) => {
        setTimeout(() => {cb(null, 'B')
        }, 250)}
    const opC = (cb) => {
        setTimeout(() => {
            cb(null, 'C')
            }, 125)}
```
Call the functions in such a way thatAthenBthenCis printed out.