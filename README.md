# Trips-JS
Ok
<pre>
  let query = {
  a: 1,
  c: 3,
  e: 5,
  id: ['A1342', 'Be345', 'C4325225'],

}
var queryString = Object.keys(query).map(key => {
  if (query[key].constructor === Array) {
    var theArrSerialized = ''
    for (let singleArrIndex of query[key]) {
      theArrSerialized = theArrSerialized + singleArrIndex + '%2C'
    }
    return key + '=' + theArrSerialized.substring(0, theArrSerialized.length - 3);
  }
  else {
    return key + '=' + query[key] + '&'
  }
}
).join('');
console.log('?' + queryString)
</pre>
