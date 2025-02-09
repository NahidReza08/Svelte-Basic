<script>
    import Course from './Course.svelte';

    const course1 = {course: 'Svelte (Basic)', instructor:'NAHID REZA'}
    const course2 = {course: 'Svelte (Advance)', instructor:'MD. NAHID REZA'}

  </script>
  
  <Course />

  <Course course={course1.course} instructor={course1.instructor} />

  <Course {...course2} />
  