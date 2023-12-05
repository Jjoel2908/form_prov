# form_prov
FORMULARIO PARA GESTIÓN DE TROPAS


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"
    />

    <title>Document</title>
  </head>
  <body>
    <form
      method="post"
      id="formReporteIncidente"
      enctype="multipart/form-data"
      autocomplete="off"
    >
      <div class="modal-body">
        <div class="row">
          <!-- Fecha y hora del evento -->
          <div class="form-group col-sm-6">
            <i class="fa fa-calendar"></i>
            <label for="fecha_hora_evento"
              >Fecha y Hora del Evento <span class="red">*</span></label
            >
            <input
              type="datetime-local"
              name="fecha_hora_evento"
              id="fecha_hora_evento"
              class="form-control"
              required="required"
            />
          </div>

          <!-- Tipo de evento -->
          <div class="form-group col-sm-6">
            <i class="fa fa-exclamation-triangle"></i>
            <label for="tipo_evento"
              >Tipo de Evento <span class="red">*</span></label
            >
            <select
              name="tipo_evento"
              id="tipo_evento"
              class="form-control"
              required="true"
            >
              <option value="aceleracion_brusca">Aceleración Brusca</option>
              <option value="frenada_repentina">Frenada Repentina</option>
              <option value="giro_agresivo">Giro Agresivo</option>
              <option value="robo">Robo de Unidad</option>
              <option value="colision">Colisión</option>
              <option value="es_area">Entrada / Salida de Área Predefinida</option>
              <option value="camara_tapada">Cámara Tapada</option>
              <option value="otro">Otro</option>
            </select>
          </div>

          <!-- Unidad o vehículo involucrado -->
          <div class="form-group col-sm-6">
            <i class="fa fa-car"></i>
            <label for="unidad_vehiculo"
              >Unidad o Vehículo Involucrado <span class="red">*</span></label
            >
            <input
              type="text"
              name="unidad_vehiculo"
              id="unidad_vehiculo"
              class="form-control"
              required="required"
            />
          </div>

          <!-- Identificación del conductor -->
          <div class="form-group col-sm-6">
            <i class="fa fa-user"></i>
            <label for="id_conductor">Identificación del Conductor</label>
            <input
              type="text"
              name="id_conductor"
              id="id_conductor"
              class="form-control"
            />
          </div>

          <!-- Ubicación -->
          <div class="form-group col-sm-12">
            <i class="fa fa-map-marker"></i>
            <label for="ubicacion">Ubicación <span class="red">*</span></label>
            <input
              type="text"
              name="ubicacion"
              id="ubicacion"
              class="form-control"
              required="required"
            />
          </div>

          <!-- Detalles adicionales del incidente -->
          <div class="form-group col-sm-12">
            <i class="fa fa-comment"></i>
            <label for="detalles_incidente"
              >Detalles Adicionales del Incidente</label
            >
            <textarea
              class="form-control"
              rows="3"
              name="detalles_incidente"
              id="detalles_incidente"
              placeholder="Detalles adicionales sobre el incidente"
            ></textarea>
          </div>

          <!-- Número de identificación del vehículo (VIN) -->
          <div class="form-group col-sm-6">
            <i class="fa fa-car"></i>
            <label for="vin">Número de Identificación del Vehículo (VIN)</label>
            <input type="text" name="vin" id="vin" class="form-control" />
          </div>

          <!-- Número de placa -->
          <div class="form-group col-sm-6">
            <i class="fa fa-car"></i>
            <label for="placa">Número de Placa</label>
            <input type="text" name="placa" id="placa" class="form-control" />
          </div>

          <!-- Número de serie del dispositivo de seguimiento -->
          <div class="form-group col-sm-6">
            <i class="fa fa-wifi"></i>
            <label for="numero_serie_dispositivo"
              >Número de Serie del Dispositivo de Seguimiento</label
            >
            <input
              type="text"
              name="numero_serie_dispositivo"
              id="numero_serie_dispositivo"
              class="form-control"
            />
          </div>

          <!-- Estado del conductor -->
          <div class="form-group col-sm-6">
            <i class="fa fa-user"></i>
            <label for="estado_conductor">Estado del Conductor</label>
            <select
              name="estado_conductor"
              id="estado_conductor"
              class="form-control"
            >
              <option value="alerta">Alerta</option>
              <option value="fatigado">Fatigado</option>
              <option value="distractido">Distractido</option>
              <option value="enfermo">Enfermo</option>
              <option value="emocional">Condición Emocional</option>
            </select>
          </div>

          <!-- Subir imagen del incidente -->
          <div class="form-group col-sm-6">
            <i class="fa fa-image"></i>
            <label for="imagen_incidente">Imagen del Incidente</label>
            <input
              type="file"
              name="imagen_incidente"
              id="imagen_incidente"
              class="form-control-file"
            />
            <small class="form-text text-muted"
              >Sube una imagen relacionada con el incidente (opcional).</small
            >
          </div>
        </div>
      </div>

      <div class="modal-footer">
        <button
          type="submit"
          class="btn btn-success btn-sm w-xs btn-rounded waves-effect waves-dark"
        >
          <i class="md md-save"></i> Guardar
        </button>
        <button
          type="button"
          class="btn btn-danger btn-sm w-xs btn-rounded waves-effect waves-dark"
          data-dismiss="modal"
        >
          <i class="md md-close"></i> Cerrar
        </button>
      </div>
    </form>

    <div class="container mt-5">
      <div class="row">
        <div class="col-md-8 offset-md-2">
          <div class="card">
            <div class="card-body">
              <h2 class="card-title text-center mb-4">
                Informe de Incidente de Tráfico
              </h2>

              <div class="incident-details">
                <h4>Detalles del Incidente:</h4>
                <p>
                  Fecha y Hora del Incidente: 4 de Diciembre de 2023, 09:30 AM
                </p>
                <p>Tipo de Evento: Colisión</p>
                <p>Número de Identificación del Vehículo (VIN): XXXXXXXXX</p>
                <p>Número de Placa: ABC123</p>
                <p>Número de Serie del Dispositivo de Seguimiento: XYZ987</p>
                <p>Código de Identificación Único en la Plataforma: ID123456</p>
                <p>Ubicación del Incidente: Calle Principal, Ciudad XYZ</p>
                <p>Estado del Conductor: Fatigado</p>
                <p>Actividades del Conductor: En Ruta</p>
                <p>Datos del Sensor o Dispositivo: Número de Serie: XYZ987, Tipo de Sensor: GPS</p>
                <!-- ... Otros detalles del incidente ... -->

                <h4>Descripción del Incidente:</h4>
                <p>Se registró un evento de colisión a las 09:30 AM en la intersección de la Calle 
                    Principal en la Ciudad XYZ. El vehículo con VIN XXXXXXXXX, identificado con la 
                    placa ABC123, estuvo involucrado en una colisión leve con otro vehículo detenido 
                    en un semáforo. La condición del conductor se informó como fatigada. 
                    El dispositivo de seguimiento identificado con el número de serie XYZ987 detectó este incidente.</p>
                <!-- ... Más detalles del incidente ... -->

                <h4>Detalles Adicionales:</h4>
                <p>Se adjunta una imagen del incidente que muestra el lugar y los vehículos involucrados. El conductor, 
                    a pesar de estar fatigado, no sufrió lesiones graves ni se reportaron daños significativos en los 
                    vehículos. Se realizará un seguimiento para evaluar el estado de alerta del conductor en el momento 
                    del incidente y se implementarán medidas preventivas para evitar futuras colisiones debido a la fatiga del conductor.</p>
                <!-- ... Otros detalles adicionales ... -->
              </div>

              <hr />
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</html>
