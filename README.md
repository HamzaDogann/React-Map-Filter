Bu proje, kimya alanında önemli başarılar elde etmiş bazı insanları göstermektedir. React kullanarak, `filter` ve `map` fonksiyonlarıyla veri manipülasyonunu öğrenmeyi hedeflemektedir.

## Filter ve Map Nedir?

- **Filter Fonksiyonu:** `filter` fonksiyonu, bir dizide belirli bir koşulu sağlayan öğeleri filtrelememize olanak tanır. Bu projede, kimyagerlerin listesinden sadece kimyagerleri filtrelemek için kullanılmıştır.

- **Map Fonksiyonu:** `map` fonksiyonu, bir dizideki her öğe üzerinde döngü yapmamıza ve her öğe için belirli bir işlem gerçekleştirmemize olanak tanır. Bu projede, kimyagerlerin listesindeki her bir kimyager için bir liste öğesi oluşturmak için kullanılmıştır.

## Örnek Kodlar

```jsx
import { people } from './data.js';
import getImageUrl from './utils.js';

const chemists = people.filter(person => person.profession === "chemist");

const listItems = chemists.map(person => (
  <li key={person.id}>
    <img
      src={getImageUrl(person)}
      alt={person.name}
    />
    <p>
      <b>{person.name}:</b>
      {' '} Bir {person.profession}, {' '}
      {person.accomplishment} ile tanınıyor.
    </p>
  </li>
));
