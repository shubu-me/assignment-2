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
output
[2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97]
