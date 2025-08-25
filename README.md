# 🚍 Automating Employee Transport Routing with Python + ML  

## 🌟 Introduction  
Employee transport routing is not just about finding the shortest path — it’s about balancing **cost-efficiency**, **safety**, and **compliance**.  
Every day, supervisors must make hundreds of routing decisions that combine **zone logic**, **vehicle allocation**, and **special constraints** (escorts, medical cases, restricted roads).  

In this project, I built an **end-to-end routing engine in Python**, combining:  
- **Engineered zone frameworks** (backbone of clubbing rules),  
- **Pattern learning from historical supervisor trails**,  
- **Rule-based seater allocation logic**,  
- **Validation & audit dashboards in Power BI + route map visuals in Folium**,  
- **ML experiments (scikit-learn)** to test the learnability of supervisor routing patterns.  

---

## 🛠️ Solution Design  

1. **Engineered a zone framework** ✅  
   - Developed a coding system from 750+ nodal points.  
   - Defined how areas can be clubbed together.  
   - Replaced blind clustering with **business-aware grouping**.  

2. **Pattern learning from supervisor trails** ✅  
   - Analysed the Week_Routes dataset to learn how supervisors actually merged/split zones.  
   - Encoded these “trail clubbing” patterns into the routing engine.  
   - Optimized tail routes (≤4 employees) by aligning them with historical patterns.  

3. **Rule-based routing engine (Python)**  
   - Sorted employees by `Shift`, `Zone`, `IN/OUT`, `Distance`.  
   - Allocated vehicles in descending order: **12 → 6 → 4 seaters**.  
   - Generated predicted tripsheets automatically.  

4. **Validation & audit**  
   - Verified **no over-capacity, zone misalignment, or IN/OUT mixing**.  
   - Compared **Predicted vs Actual** routes shift-wise/day-wise.  
   - Exported results to Excel/Power BI and generated **Folium route maps**.  

5. **ML experiments (scikit-learn, LightGBM planned)**  
   - Tested KNN to predict tripsheet allocations directly.  
   - Found ~50% accuracy with limited features, showing supervisor discretion (escort, vendor, special cases) must be modeled.  

---

## 📊 Results  

- **Employee-to-route assignment accuracy**: ~90%  
- **Operational discretion (~10%)**:  
  - Restricted roads → larger vehicles not feasible  
  - Medical cases → smaller vehicles only  
  - Escort provisions → mandatory seat reserved at night  
  - Special cases → VIPs, senior management, unique requests  

✅ 90% automation + 10% supervisor discretion = **100% operational feasibility**  

---

## 🏆 Achievements  

- **Engineered a zone framework** → backbone of routing.  
- **Implemented pattern learning** → captured supervisor clubbing logic.  
- Built the **first Python-based end-to-end routing pipeline** with validation & dashboards.  
- Applied **Python + ML (pandas, scikit-learn, folium)** to automate routing decisions.  
- Quantified ~10% of routes as shaped by **operational constraints**, proving the need for discretion.  
- Created **map visuals** for business-friendly validation.  

---

## 🚀 Next Steps  

- Enrich dataset with escort, vendor, gender, and SLA features.  
- Train a **LightGBM model** to replicate supervisor tripsheets directly.  
- Add **zone adjacency logic** to merge tails efficiently.  

---

## 📌 Conclusion  

This project demonstrates that:  
- **Zones provide structure**,  
- **Pattern learning adds nuance**,  
- **Supervisor discretion ensures compliance**.  

Together they deliver **100% routing coverage**:  
- 90% automated in Python,  
- 10% via supervisor discretion.  

> In applied data science, true success isn’t just accuracy — it’s about building systems that are both **data-driven and operationally feasible**.  

---

