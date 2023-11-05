# codigo_servibles
Codigo que tal vez deba de utilizar algun día


Obtener datos de una api y ponerlo en una tabla
<table id="datatable" class="display">
        <thead>
            <tr>
                <th>id</th>
                <th>conocimiento</th>
            </tr>
        </thead>
        <tbody>
            <!-- Aquí se agregarán las filas con jQuery -->
        </tbody>
    </table>
$(document).ready(function() {
    $.ajax({
        type:'GET',
        url: "https://sga.unemi.edu.ec/api?a=areaconocimiento",
        success: function(data){
            for(e in data.areasconocimiento){
                id = data.areasconocimiento[e]['id']
                nombre = data.areasconocimiento[e]['nombre']
                linea = "<tr><td>"+id+"</td><td>"+nombre+"</td></tr>"
                $(linea).appendTo("#dataTable tbody");


Responsibe div 
flex wart: wart
            }
            $('#dataTable').DataTable();
        }
    })
});
