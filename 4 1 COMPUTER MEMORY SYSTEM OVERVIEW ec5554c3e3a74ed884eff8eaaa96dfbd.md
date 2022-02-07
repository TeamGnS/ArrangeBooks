# 4.1 COMPUTER MEMORY SYSTEM OVERVIEW

## Characteristics of Memory Systems

![Untitled](4%201%20COMPUTER%20MEMORY%20SYSTEM%20OVERVIEW%20ec5554c3e3a74ed884eff8eaaa96dfbd/Untitled.png)

### Internal Memory와 관련된 세 가지 개념

- **단어(Word)**
    - memory organization의 '자연스러운' 단위
    - number을 표현하기 위해 사용되는 bit들의 수 또는 instruction의 길이와 같음
    - ex. Intel x86 architecture
        - 매우 다양한 instruction 길이
        - byte의 배수로 표현
        - 단어의 길이는 32bit
- **주소지정 단위(Addressable units)**
    - 대부분의 시스템은 byte 단위의 주소지정 단위 허용
    - $2^A=N$
        
        *A*: 주소의 길이 (bit)
        
        *N*: 주소지정 단위의 수
        
- 전송의 단위
    - Main memory에서는 한 번에 읽고 쓸 수 있는 bit의 수
    - External memory에서 data의 전송 단위는 **block**

### Methods of Accessing Units of Data

![Untitled](4%201%20COMPUTER%20MEMORY%20SYSTEM%20OVERVIEW%20ec5554c3e3a74ed884eff8eaaa96dfbd/Untitled%201.png)

- **Sequential access**
    - Tape unit
- **Direct access**
    - Disk unit
- **Random access**
    - Main memory, Cache system

<aside>
💡 **Associative**

- Cache memory

**content addressable, parallel search!**

</aside>

### Performance을 나타내는 3가지 parameters

- **Access time (latency)**
    - 읽거나 쓰는 동작을 수행하는데 걸리는 시간
    - 주소가 memory에 도착하는 순간 → data가 저장되거나 읽혀지는 순간
- **Memory cycle time**
    - 주로 Random-Access Memory에 적용
    - system bus와 관계가 있으며, processor와는 무관
- **Transfer rate (전송률)**
    - data가 memory로 전송되어 들어가거나 나오는 비율
    - 1 / (*cycle time*)
    - Non-Random-Access Memory
        
        ![Untitled](4%201%20COMPUTER%20MEMORY%20SYSTEM%20OVERVIEW%20ec5554c3e3a74ed884eff8eaaa96dfbd/Untitled%202.png)
        

## The Memory Hierarchy

- **Memory 구현을 위해 사용된 기술들 속에서 성립되는 관계들**
    - access 속도가 빨라짐 → bit 당 가격은 높아짐
    - 용량 커짐 → bit당 가격은 낮아짐
    - 용량 커짐 → access 속도는 느려짐

![상위 계층일수록 빠르고, 작으며, 비싸다.](4%201%20COMPUTER%20MEMORY%20SYSTEM%20OVERVIEW%20ec5554c3e3a74ed884eff8eaaa96dfbd/Untitled%203.png)

상위 계층일수록 빠르고, 작으며, 비싸다.

1. **bit당 가격 감소**
2. **용량 증가**
3. **access 시간 증가**
4. **processor에 의해 memory가 access되는 빈도 감소**