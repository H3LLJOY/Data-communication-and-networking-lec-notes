# 📡 Switching and Network Types

## 🔄 Types of Network

### 🔹 Unswitched

- **Point-to-point**
- **Multi-point**
- **Broadcast**

### 🔹 Switched

- **Data** passes through one or more **intermediate nodes** between the sender and receiver.

## ❓ Why Switched Networks?

1. **Unswitched Networks Complexity**:
   - **3 nodes**: 3 links
   - **4 nodes**: 6 links
   - **5 nodes**: 10 links
   - **10 nodes**: ? (many links)
2. **Advantages**:
   - **Cost-effective**: Not all nodes need to be **directly interconnected**, reducing costs.
   - **Range**: Suitable for vast, spread-out networks where broadcasting signals is impractical.
   - **Efficiency**: Signals can be **switched** from sender to receiver.

## 💡 Switching: Abstract Model

- **Number of inputs/outputs**: Varies from few (e.g., 4 or 8) to huge (e.g., 100K).

## ❗ Why Switching?

- To ensure signals reach the **correct destination**.
- Necessary when the source and destination are **not directly connected** (e.g., travelling by bus).
- Beneficial for **large networks** in size or number of stations.

## 🔀 Routing and Switching

- **Routing**: Identifies the route data traverses from source to destination.
- **Switching**: Transfers data from one network/link to another.

## 🔹 Types of Switching

### 🔸 Circuit Switching

- **Dedicated Communications Path**: Pre-allocated between caller, callee, and all intermediate nodes.
- **Resource Allocation**: Once established, the circuit capacity must be paid for, used or not.
- **Low Transmission Delays**: Once the route is set up, though it cannot be optimized.
- **Suitability**: Ideal for human-to-human telephone communications; less suited for computer communications.
- **Types of Circuit Switching**:
  - **Space-division switching**: Each call takes a different path.
  - **Time-division switching**: Each call is divided into small pieces, each piece assigned a time-slot, and switched independently.

#### Space Division Switch

- Each sample takes a **different path**, based on the destination.
- **Crossbar Switch**: Simple space-division switch. **Crosspoints** can be turned **on or off**.

#### Time-Division Switching

- **Multiplexor**: Aggregates sessions, with N input lines and output running N times faster.
- **Demultiplexor**: Distributes sessions, with one input line and N outputs running N times slower.
- Can cascade multiplexors.

### 🔸 Message Switching

- Entire messages sent **store-and-forward, hop-by-hop**.
- **Intermittent Progress**: Message progresses as each hop becomes available.
- **Timing**: End-to-end delivery time isn't guaranteed.
- **Issues**: Very long messages can **hog buffer space** and links.

### 🔸 Packet Switching

- Network comprises a set of **nodes** (switches or routers), connected by **links** (point-to-point, broadcast).
- Data stream is divided into **packets**, each with data and a header.
- Data sent from one **host** to another, with intermediate stations **switching** each packet through links.

#### Types of Packet Switching

- **Virtual Circuit Switching**:
  - **Connection Setup**: Before data transfer, packets travel a pre-chosen route.
  - Virtual Circuit Identifier (VCI): Each packet assigned a unique identifier.
- **Datagram Switching**:
  - **Independent Routing**: Packets routed independently, without initial setup costs.
  - **Adaptive**: Handles node and link failures, though packets might arrive out of order.
  - Uses a **routing table** based on the destination address, which remains unchanged during the journey.
- **Label Switching**:
  - **Edge Routing & Core Switching**: Each packet received is attached with a label.
  - **Core Switch**: Routes packets based on labels, substituting a new label for the next hop.

## 🔗 Label Switched Network

### Visualizing Label Switched Network

**Packet Flow**:

| **Packet** | **Initial Label** | **New Label** |
| ---------- | ----------------- | ------------- |
| P1         | Label A           | Label B       |
| P2         | Label X           | Label Y       |

## 📑 Summary

- **Types of Network**: Unswitched vs. Switched.
- **Switching Mechanisms**:
  - Circuit Switching: Space and Time Division.
  - Message Switching.
  - Packet Switching: Virtual Circuit, Datagram, Label.

