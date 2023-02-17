# assignment-2
fn main() {
    let mut primes = Vec::new();
    primes.push(2);
    let mut found = false;
    for n in 3..100 {
        for prime in &primes {
            if n % prime == 0 {
                found = true;
                break;
            }
        }
        if found == false {
            primes.push(n);
        }
        found = false;
    }
    println!("{:?}", primes);
}
