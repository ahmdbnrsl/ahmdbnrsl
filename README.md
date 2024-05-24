## ABOUT ME
Helle my name is Ahmad Beni Rusli.

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
