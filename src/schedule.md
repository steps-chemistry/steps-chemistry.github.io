---
layout: base.njk
title: Course Schedule
---

# Course Schedule

Below is the complete schedule for our 7-week summer course (June 29 - August 14). 

## Quick Navigation

<div class="week-nav">
  <button onclick="showWeek(1)" class="week-btn">Week 1</button>
  <button onclick="showWeek(2)" class="week-btn">Week 2</button>
  <button onclick="showWeek(3)" class="week-btn">Week 3</button>
  <button onclick="showWeek(4)" class="week-btn">Week 4</button>
  <button onclick="showWeek(5)" class="week-btn">Week 5</button>
  <button onclick="showWeek(6)" class="week-btn">Week 6</button>
  <button onclick="showWeek(7)" class="week-btn">Week 7</button>
  <button onclick="showToday()" class="today-btn">Today</button>
</div>

## Week 1 (June 29 - July 4)

<div id="week-1" class="week-section">

| Day | Date | Topics | 
|-----|------|-------------|
| 1 | Sunday, June 29 | **Program orientation (no class)** |  |
| 2/3 | Monday/Tuesday, June/July 30/1 |  Course overview. Math and Physics Fundamentals. |
| 4/5 | Wednesday/Thursday, July 2/3 | Atomic Structure. |

</div>

## Week 2 (July 5 - July 11)

<div id="week-2" class="week-section">

| Day | Date | Topics | 
|-----|------|-------------|
| 6/7 | Saturday/Sunday, July 5/6 | Periodic table, Lewis Diagrams, and VSEPR. |  
| 8/9 | Monday/Tuesday, July 7/8 | Inter Molecular Forces, Properties of Substances, Chromatography, Distillation and Spectroscopy. |  
| 10/11 | Wednesday/Thursday, July 9/10 | Stoichiometry, Yield and Compound Formation. |  

</div>

## Week 3 (July 12 - July 18)

<div id="week-3" class="week-section">

| Day | Date | Topic | 
|-----|------|-------------|
| 12/13 | Saturday/Sunday, July 12/13 | Continuum Hypothesis, Kinetic Molecular Theory, Ideal Gas Law, and Equations of State. |  
| 14/15 | Monday/Tuesday, July 14/15 | First Law, Enthalpies, Heat of Reaction, and Hess' Law. |  
| 16/17 | Wednesday/Thursday, July 16/17 | Conduction, Convection, Radiation, and Specific Heat Capacity. |  


</div>

## Week 4 (July 19 - July 25)

<div id="week-4" class="week-section">

| Day | Date | Topic | 
|-----|------|-------------|
| 18/19 | Saturday/Sunday, July 19/20 | Intro to Kinetics, Arrhenius Law, Activation Energy, and Steady State Approximation. |  
| 20/21 | Monday/Tuesday, July 21/22 | Law of Mass Action, Factors Affecting Rates (Catalysts) and Radioactive Decay. |  
| 22/23 | Wednesday/Thursday, July 23/24 | Reversible Reactions, Equilibrium, and Equilibrium Constants and Le Chatelier. |  


</div>

## Week 5 (July 26 - August 1)

<div id="week-5" class="week-section">

| Day | Date | Topic | 
|-----|------|-------------|
| 24/25 | Saturday/Sunday, July 26/27 | Acids and Bases, Bronsted-Lowry,and  Ionic Equations. |  
| 26/27 | Monday/Tuesday, July 28/29 | pH and pOH, Conjugates and Buffers. |  
| 28/29 | Wednesday/Thursday, July 30/31 | Redox and Oxidation numbers. |  


</div>

## Week 6 (August 2 - August 8)

<div id="week-6" class="week-section">

| Day | Date | Topic | 
|-----|------|-------------|
| 30/31 | Saturday/Sunday, August 2/3 | The Second Law of Thermodynamics and Gibbs Free Energy. |  
| 32/33 | Monday/Tuesday, August 4/5 | Galvanic Cell, Electrolysis and Nernst Equation. |  
| 34/35 | Wednesday/Thursday, August 6/7 | Intro to Organic, Alkanes, Alkenes, Alkynes, Isomers: Structural and Optical. |  


</div>

## Week 7 (August 9 - August 15)

<div id="week-7" class="week-section">

| Day | Date | Topic | 
|-----|------|-------------|
| 36/37 | Saturday/Sunday, August 9/10 | Functional Groups; Alcohols, Ethers, Aldehydes, Ketones, Carboxylic Acids, Esters and Amines. |  
| 38/39 | Monday/Tuesday, August 11/12 | Addition, Cracking, Nucleophiles and Electrophiles. |  
| 40/41 | Wednesday/Thursday, August 13/14 | Interactive Q/A and Review. |  


</div>

<script>
// Week navigation functionality
function showWeek(weekNumber) {
    // Hide all week sections
    const weekSections = document.querySelectorAll('.week-section');
    weekSections.forEach(section => {
        section.style.display = 'none';
    });
    
    // Hide all week headers
    const weekHeaders = document.querySelectorAll('h2');
    weekHeaders.forEach(header => {
        if (header.textContent.includes('Week')) {
            header.style.display = 'none';
        }
    });
    
    // Show selected week
    const selectedWeek = document.getElementById(`week-${weekNumber}`);
    if (selectedWeek) {
        selectedWeek.style.display = 'block';
    }
    
    // Show the corresponding header
    const weekHeadersArray = Array.from(document.querySelectorAll('h2'));
    const targetHeader = weekHeadersArray.find(header => 
        header.textContent.includes(`Week ${weekNumber}`)
    );
    if (targetHeader) {
        targetHeader.style.display = 'block';
    }
    
    // Update active button
    document.querySelectorAll('.week-btn').forEach(btn => btn.classList.remove('active'));
    event.target.classList.add('active');
}

function showToday() {
    const today = new Date();
    const startDate = new Date('2024-06-29'); // Actual start date
    const daysDiff = Math.floor((today - startDate) / (1000 * 60 * 60 * 24));
    
    if (daysDiff >= 0 && daysDiff <= 40) {
        let weekNumber;
        if (daysDiff < 5) {
            weekNumber = 1; // First week (Sunday-Friday)
        } else {
            weekNumber = Math.floor((daysDiff - 5) / 7) + 2; // Subsequent weeks (Saturday-Friday)
        }
        showWeek(weekNumber);
        
        // Highlight today's row
        const todayRow = document.querySelector(`tr[data-day="${daysDiff + 1}"]`);
        if (todayRow) {
            todayRow.classList.add('today');
        }
    } else {
        showWeek(1); // Show week 1 if before start date
    }
}

// Initialize page
document.addEventListener('DOMContentLoaded', function() {
    // Show current week by default
    const today = new Date();
    const startDate = new Date('2024-06-29'); // Actual start date
    const daysDiff = Math.floor((today - startDate) / (1000 * 60 * 60 * 24));
    
    if (daysDiff >= 0 && daysDiff <= 40) {
        let weekNumber;
        if (daysDiff < 5) {
            weekNumber = 1; // First week (Sunday-Friday)
        } else {
            weekNumber = Math.floor((daysDiff - 5) / 7) + 2; // Subsequent weeks (Saturday-Friday)
        }
        showWeek(weekNumber);
    } else {
        showWeek(1); // Default to week 1 if before start date
    }
});
</script>

<style>
.week-nav {
    margin: 20px 0;
    text-align: center;
}

.week-btn, .today-btn {
    margin: 5px;
    padding: 10px 15px;
    border: 2px solid #007bff;
    background: white;
    color: #007bff;
    border-radius: 5px;
    cursor: pointer;
    transition: all 0.3s ease;
}

.week-btn:hover, .today-btn:hover {
    background: #007bff;
    color: white;
}

.week-btn.active {
    background: #007bff;
    color: white;
}

.today-btn {
    background: #0056b3;
    border-color: #0056b3;
    color: white;
}

.today-btn:hover {
    background: #004085;
    border-color: #004085;
}

.week-section {
    display: none;
    margin-bottom: 30px;
}

.week-section:first-of-type {
    display: block;
}

tr.today {
    background-color: #fff3cd !important;
    border-left: 4px solid #ffc107;
}

h2 {
    margin-top: 30px;
    padding: 15px;
    background: #f8f9fa;
    border-radius: 5px;
    border-left: 4px solid #007bff;
}

</style>




