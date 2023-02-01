<template>
    <div>
        <h1>Employee List</h1>

        <table>
            <tr>
                <td>Name</td>
                <td>Salary</td>
                <td>Age</td>
            </tr>
            <tr v-for="item in list" :key="item.id">
                <td>{{ item.employee_name }}</td>
                <td>{{ item.employee_salary }}</td>
                <td>{{ item.employee_age }}</td>
            </tr>
        </table>
    </div>
</template>

<script>


    export default{
        name: "API_Data",
    }
</script>