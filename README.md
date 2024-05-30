## `Introduction`

Hello, my name is Ahmad Beni Rusli. I was born in Cilacap on July 23, 2005. Currently, I live in Rt03 RW 05 Tinggarjaya village, Sidareja subdistrict, Cilacap district.

Since I was a child, I have had a great interest in the world of art and technology. This can be seen from my hobbies of painting and coding.

For me, painting is a way to express myself and pour out my creativity. While coding, I consider it an art to build something useful and that can help many people.

My interest in art and technology has led me to my dream of becoming a Fullstack Web Developer. I want to combine my skills in design art and programming to create beautiful and functional websites.

I am confident that with hard work and dedication, I can achieve my goals and become a successful Fullstack Web Developer.

Thank you for your attention.
```typescript
interface Address {
    street: string;
    city: string;
}

interface Hobbies {
    [index: number]: string;
}

interface DetailEducations {
    name: string;
    address: string;
    level: string;
    year: string;
}

interface Educations {
    [index: number]: DetailEducations;
}

interface FavouritesFoods {
    [index: number]: string;
}

interface Person {
    name: string;
    birth: string;
    address: Address;
    hobbies: Hobbies;
    educations: Educations;
    favouritesFoods: FavouritesFoods;
}

class MyDetail<Type extends Person> {
    constructor(public myDetail: Type) {}
}

const myDetail = new MyDetail<Person>({
    name: "Ahmad Beni Rusli",
    birth: "Cilacap, 23 July 2005",
    address: {
        street: "Jln. Cipari no 4",
        city: "Cilacap"
    },
    hobbies: [
        "Coding",
        "Drawing",
        "Workout",
        "Sleeping"
    ],
    educations: [
        {
            name: "MI Islamiyah",
            address: "Jln. Cipari no 4, Tinggarjaya",
            level: "elementary school",
            year: "2011 - 2017"
        },
        {
            name: "MTs Darul Ulum 02",
            address: "Jln. Makam Pahlawan, Tinggarjaya",
            level: "Junior high school",
            year: "2017 - 2020"
        },
        {
            name: "SMK Darul Ulum",
            address: "Jln. Makam Pahlawan, Tinggarjaya",
            level: "Vacational High School",
            year: "2020 - 2023"
        }
    ],
    favouritesFoods: [
        "Fried Chicken",
        "Ice Cream"
    ]
});
```
