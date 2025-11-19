```Python
from dataclasses import dataclass
from typing import Optional, List

@dataclass
class Person:
    first_name: str = "Wayne"
    last_name: str = "Cole"
    age: int = 22
    email: Optional[str] = "waynecole339@gmail.com"
    website: Optional[str] = "https://waynecole.info"
    languages: List[str] = ["C", "C++", "Go", "Typescript", "Python", "Lua", "Bash"]
    
    @property
    def full_name(self) -> str:
        return f"{self.first_name} {self.last_name}"
    
    @property
    def age(self) -> int:
        return self.age

# Usage example:
person = Person(
    first_name="Wacky",
    last_name="404", 
    age=22,
    email="wcole@btytechnology.com"
)

print(person.full_name)  # Wacky 404
print(person.age)        # 22
```
