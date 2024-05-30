## `Introduction`

Hello, my name is Ahmad Beni Rusli. I was born in Cilacap on July 23, 2005. Currently, I live in Rt03 RW 05 Tinggarjaya village, Sidareja subdistrict, Cilacap district.

Since I was a child, I have had a great interest in the world of art and technology. This can be seen from my hobbies of painting and coding.

For me, painting is a way to express myself and pour out my creativity. While coding, I consider it an art to build something useful and that can help many people.

My interest in art and technology has led me to my dream of becoming a Fullstack Web Developer. I want to combine my skills in design art and programming to create beautiful and functional websites.

I am confident that with hard work and dedication, I can achieve my goals and become a successful Fullstack Web Developer.

Thank you for your attention.
```json
{
    "name": "Ahmad Beni Rusli",
    "age": 19,
    "birth": "Cilacap, 23 July 2005",
    "address": { "street": "Jln Cipari no 4", "city": "Cilacap" },
    "hobbies": [ "drawing", "coding" ],
    "educations": [
        { "level": "vacation high school", "name": "SMK Darul Ulum" }
        { "level": "junior high school", "name": "MTs Darul Ulum 02" }
    ]
}
```
```typescript
//index.ts
import Data from './data.json' assert { type: 'json' };

interface Address { street: string, city: string }
interface Educations { level: string, name: string }
interface Detail<A extends Address, E extends Educations> {
    name: string;
    age: number;
    birth: string;
    address: A;
    hobbies: Array<string>;
    educations: Array<E>;
}

class About
<T extends Detail<Address, Educations>
{
    constructor( public aboutMe: T ) {}

    get Name(): string { return this.aboutMe.name }
    set Name(name: string): void { this.aboutMe.name = name }
}

const about =
    new About<Detail<Address, Educations>>(Data);
console.info("Hello " + about.Name);
```
