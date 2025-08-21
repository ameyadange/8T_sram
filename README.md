## Project Overview

This project presents the design and simulation of an 8-transistor Static Random Access Memory (SRAM) cell using LTSpice circuit simulation software. The 8T SRAM cell improves upon the traditional 6T SRAM design by providing enhanced stability, better noise margins, and improved read/write characteristics.

## 8T SRAM Cell Architecture

### Transistor Configuration

The 8T SRAM cell consists of:

1. **Storage Core (4 transistors):** Two cross-coupled inverters forming a bistable latch
2. **Write Access (2 transistors):** Write access transistors controlled by write word line (WWL)
3. **Read Access (2 transistors):** Read access transistor and read buffer controlled by read word line (RWL)

### Circuit Topology

```
VDD ---|P1|----+-------|P2|--- VDD
           |    |           |
          Q|    |           |QB
           |    |           |
       |N1|----+-------|N2|
           |           |
       |N3|           |N4|
           |           |
          WBL         WBLB
           |           |
          WWL---------WWL

           |
       |N5|
           |
          RBL
           |
       |N6|
           |
          RWL
```

## Advantages over 6T SRAM

1. **Read Stability:** Separate read path eliminates read disturb issues and improves Static Noise Margin (SNM)
2. **Write Performance:** Dedicated write access transistors provide better write margins and faster operations
3. **Power Efficiency:** Lower leakage current and reduced dynamic power during read operations
4. **Process Variation Tolerance:** More robust against PVT variations in advanced technology nodes

## Simulation Setup in LTSpice

### Key Simulations

1. **DC Analysis:** Static Noise Margin calculation and butterfly curve generation
2. **Transient Analysis:** Read/write operation timing and data retention verification
3. **AC Analysis:** Frequency response and stability analysis

## Performance Metrics

### Expected Results
- SNM Enhancement: 20-30% improvement over 6T SRAM
- Leakage Reduction: 10-15% reduction in standby power
- Area Overhead: Approximately 25-30% larger than 6T cell

## Design Trade-offs

**Benefits:**
- Enhanced read stability and write ability
- Better noise margins and power efficiency
- Improved process variation tolerance

**Costs:**
- Increased area overhead
- Higher design complexity
- Additional routing requirements

## Conclusion

The 8T SRAM cell represents a significant advancement over traditional 6T designs, offering improved stability and performance at the cost of increased area. The LTSpice simulation framework enables comprehensive analysis and optimization of the cell design for specific applications where reliability and performance are paramount.

## References

1. IEEE Transactions on Very Large Scale Integration (VLSI) Systems - 8T SRAM Design Papers
2. International Solid-State Circuits Conference (ISSCC) - Memory Design Sessions
3. LTSpice User Manual and Documentation
4. BSIM Model Documentation for Advanced Technology Nodes

5. Project by Ameya Dange.
