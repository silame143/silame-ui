<template>
    <v-card>
        <v-card-title>
            Students
            <v-spacer></v-spacer>
            <v-text-field v-model="search" append-icon="mdi-magnify" label="Search Student" single-line
                hide-details></v-text-field>
        </v-card-title>
        <v-data-table :headers="headers" :items="StudentData" :search="search">
            <template slot="item.actions" slot-scope="{item}">
                <v-btn color="blue accent-4"> DELETE</v-btn>
                <v-btn color="blue accent-4"> EDIT</v-btn>
            </template>
        </v-data-table>

    </v-card>
</template>
<script>
export default {
    data() {
        return {
            search: '',
            headers: [
                {
                    text: 'ID',
                    align: 'start',
                    sortable: false,
                    value: 'StudentID',
                },
                { text: 'First Name', value: 'First_Name' },
                { text: 'Last Name', value: 'Last_Name' },
                { text: 'Middle Initial', value: 'Middle_Initial' },
                { text: 'Course', value: 'Course' },
                { text: 'Year', value: 'Year' },
                { text: '', value: "actions" }
            ],
            StudentData: [
                {

                    First_Name: 'ShielaMae',
                    StudentID: '22-00657',
                    Last_Name: 'Mortega',
                    Middle_Initial: 'L.',
                    Course: 'BSIT',
                    Year: '3',
                },
                
                {

                    First_Name: 'ShielaMae',
                    StudentID: '22-00657',
                    Last_Name: 'Mortega',
                    Middle_Initial: 'L.',
                    Course: 'BSIT',
                    Year: '3',
                },
                {

                    First_Name: 'ShielaMae',
                    StudentID: '22-00657',
                    Last_Name: 'Mortega',
                    Middle_Initial: 'L.',
                    Course: 'BSIT',
                    Year: '3',
                },
                

            ],
        }
    },
}
</script>