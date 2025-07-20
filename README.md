```Python
from dataclasses import dataclass
from typing import Optional, List

@dataclass
class Person:
    first_name: str = Wayne
    last_name: str = Cole
    age: int = 22
    email: Optional[str] = waynecole339@gmail.com
    website: Optional[str] = https://waynecole.info
    languages: List[str] = ["C", "C++", "Go", "Typescript", "Python"]
    
    @property
    def full_name(self) -> str:
        return f"{self.first_name} {self.last_name}"
    
    @property
    def age(self) -> int:
        return f"{self.age}"

# Usage example:
person = Person(
    first_name="Wacky",
    last_name="Scales", 
    age=22,
    email="fitguy@productive.com"
)

print(person.full_name)  # Wacky Scales
print(person.age)        # 22
```
