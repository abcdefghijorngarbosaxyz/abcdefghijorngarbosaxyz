```rust
mod about {
    pub struct Me {
        pub fn get_current_workplace() -> Workplace {
            Workplace {
                company: "Home".to_string(),
                position: "Web Developer".to_string(),
            }
        }
    
        pub fn get_daily_knowledge() -> Vec<&'static str> {
            vec![
                "Typescript",
                "Javascript",
                "Python",
                "Java",
                "Rust",
                "Assembly",
                "C",
            ]
        }
    
        pub fn get_future_goal() -> &'static str {
            "To build scalable and efficient web applications."
        }
    }

    pub struct Workplace {
        pub company: String,
        pub position: String,
    }
}

fn main() {
    let me = about::Me;
    
    let workplace = me.get_current_workplace();
    println!("Current Workplace: {} - {}", workplace.company, workplace.position);
    
    let daily_knowledge = me.get_daily_knowledge();
    println!("Daily Knowledge: {:?}", daily_knowledge);
    
    let future_goal = me.get_future_goal();
    println!("Future Goal: {}", future_goal);
}
