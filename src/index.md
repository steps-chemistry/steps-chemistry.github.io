---
layout: base.njk
title: Home
---

# STEPs Chemistry Course

Welcome to our high school summer chemistry course covering pre-calculus and differentiation topics. This website contains all the materials you'll need for our classes.

## Course Structure

<div class="content-grid">
<div class="content-card">

### <i class="fas fa-calendar-alt icon calendar-icon"></i> Course Schedule
View the complete daily schedule with links to topics, notes, and assignments for each class day.

[View Schedule →](/schedule/)

</div>

<div class="content-card">

### <i class="fas fa-book icon book-icon"></i> Lecture Notes
Access organized notes for each class covering fundamental concepts in pre-calculus and early calculus.

[View Notes →](/notes/)

</div>


<div class="content-card">

### <i class="fas fa-flask icon lab-icon"></i> Assignments
Hands-on exploration activities to deepen understanding of chemistry concepts.

[View Assignments →](/assignments/)

</div>
</div>

<style>
.content-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    margin: 30px 0;
}

.content-card {
    background: white;
    border: 1px solid #e9ecef;
    border-radius: 8px;
    padding: 25px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.content-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
}

.content-card h3 {
    margin-top: 0;
    margin-bottom: 15px;
    color: #333;
    display: flex;
    align-items: center;
    gap: 12px;
}

.content-card p {
    color: #666;
    margin-bottom: 20px;
    line-height: 1.5;
}

.content-card a {
    color: #007bff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.2s ease;
}

.content-card a:hover {
    color: #0056b3;
    text-decoration: underline;
}

.icon {
    font-size: 20px;
    width: 24px;
    text-align: center;
}

.calendar-icon {
    color: #007bff;
}

.book-icon {
    color: #28a745;
}

.exercise-icon {
    color: #ffc107;
}

.lab-icon {
    color: #dc3545;
}
</style>

<!-- FontAwesome CDN -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

