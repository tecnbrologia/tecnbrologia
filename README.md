-<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema de Reservas - TecnoBROlogIA</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 20px;
            background-color: #f5f5f5;
        }
        form {
            background: white;
            padding: 20px;
            border-radius: 4px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        input, select, textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .services {
            margin-top: 30px;
            background: white;
            padding: 20px;
            border-radius: 4px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>

<h2>Sistema de Reservas</h2>
<form id="reservationForm">
    <label for="name">Nombre Completo:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Correo Electrónico:</label>
    <input type="email" id="email" name="email" required>

    <label for="phone">Teléfono de Contacto:</label>
    <input type="tel" id="phone" name="phone" required>

    <label for="service">Servicio Solicitado:</label>
    <select id="service" name="service" required>
        <option value="">Seleccione un servicio</option>
        <option value="Armado de PC Gamer">Armado de PC Gamer</option>
        <option value="Activación de Windows">Activación de Windows</option>
        <option value="Limpieza de PC Gamer">Limpieza de PC Gamer</option>
        <option value="Limpieza de Notebook">Limpieza de Notebook</option>
        <option value="Cambio de Almacenamiento en Notebook">Cambio de Almacenamiento en Notebook</option>
        <option value="Cambio de RAM en Notebook">Cambio de RAM en Notebook</option>
    </select>

    <label for="date">Fecha Preferida:</label>
    <input type="date" id="date" name="date" required>

    <label for="time">Hora Preferida:</label>
    <input type="time" id="time" name="time" required>

    <label for="comments">Comentarios Adicionales:</label>
    <textarea id="comments" name="comments"></textarea>

    <button type="submit">Enviar Reserva</button>
</form>

<div class="services">
    <h3>Nuestros Servicios y Precios</h3>
    <ul>
        <li><strong>Armado de PC Gamer:</strong> $35,000 CLP</li>
        <li><strong>Activación de Windows:</strong> $25,000 CLP</li>
        <li><strong>Limpieza de PC Gamer:</strong> $20,000 CLP</li>
        <li><strong>Limpieza de Notebook:</strong> $15,000 CLP</li>
        <li><strong>Cambio de Almacenamiento en Notebook:</strong> $15,000 CLP</li>
        <li><strong>Cambio de RAM en Notebook:</strong> $10,000 CLP</li>
    </ul>
</div>

<script>
    document.getElementById('reservationForm').onsubmit = function(event) {
        event.preventDefault(); // Evita el envío del formulario
        alert('¡Gracias por tu reserva, ' + document.getElementById('name').value + '! Hemos recibido tu solicitud.');
        // Aquí puedes agregar código para enviar los datos a un servidor.
    };
</script>

</body>
</html>
