﻿ React-Map-Filter

# React Map ve Filter ile Listeleme İşlemi

Bu projede, React kullanarak bir liste öğelerini map ve filter fonksiyonlarıyla işleyerek dinamik olarak filtrelemeyi ve listelemeyi öğrendim. Bu tekniklerle veri manipülasyonunu kolayca gerçekleştirebilir ve kullanıcıların belirli kriterlere göre listeyi filtrelemesine olanak sağlayabiliriz.

## Map Fonksiyonu

`map` fonksiyonu, bir dizideki her öğe üzerinde döngü yapmamıza ve her öğe için belirli bir işlem gerçekleştirmemize olanak tanır. Bu projede, `map` fonksiyonunu kullanarak bir veri dizisindeki her öğeyi belirli bir bileşen veya içerikle eşleştirebilir ve kullanıcıya gösterebiliriz.

```jsx
const liste = [1, 2, 3, 4, 5];

const listeElemanlari = liste.map((eleman) => (
  <div key={eleman}>{eleman}</div>
));

return <div>{listeElemanlari}</div>;
