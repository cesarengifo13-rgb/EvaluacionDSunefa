<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>UNEFA Tucupido — Taller N° 1 Colaborativo: Diseño de Sistemas (20 Pts)</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- EmailJS SDK -->
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
  <!-- Fuente Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { sans: ['Inter', 'sans-serif'] },
          colors: {
            unefa: {
              navy: '#0f294a',
              blue: '#1e3a8a',
              gold: '#d97706'
            }
          }
        }
      }
    }
  </script>
  <style>
    /* Bloqueo de selección externa durante examen activo */
    body.exam-locked {
      user-select: none;
      -webkit-user-select: none;
    }
    body.exam-locked input,
    body.exam-locked textarea {
      user-select: text;
      -webkit-user-select: text;
    }

    @media print {
      body {
        background: #ffffff !important;
        color: #000000 !important;
        font-size: 10.5pt;
      }
      .no-print { display: none !important; }
      .print-only { display: block !important; }
      .print-break-inside { break-inside: avoid; }
      .shadow-xl, .shadow-lg, .shadow-md, .shadow-sm { box-shadow: none !important; }
      .border { border-color: #cbd5e1 !important; }
    }
  </style>
</head>
<body class="bg-slate-100 text-slate-800 font-sans antialiased min-h-screen flex flex-col">

  <!-- ===================================================================== -->
  <!-- NOTIFICACIONES TOAST Y MODALES (PROHIBIDO ALERT / CONFIRM)            -->
  <!-- ===================================================================== -->
  <div id="toast-container" class="fixed bottom-5 right-5 z-50 flex flex-col gap-2 max-w-sm w-full pointer-events-none no-print"></div>

  <!-- Modal Alerta Institucional (Ej. Cupo de dispositivos lleno o errores) -->
  <div id="alert-modal" class="fixed inset-0 bg-slate-900/75 backdrop-blur-sm z-50 hidden items-center justify-center p-4 no-print">
    <div class="bg-white rounded-2xl max-w-md w-full p-6 shadow-2xl border-2 border-rose-600">
      <div class="flex items-center gap-3 text-rose-700 mb-3">
        <div class="w-11 h-11 rounded-2xl bg-rose-100 text-rose-600 flex items-center justify-center shrink-0">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
          </svg>
        </div>
        <h3 id="alert-modal-title" class="text-lg font-extrabold">Acceso Denegado</h3>
      </div>
      <p id="alert-modal-message" class="text-sm text-slate-700 mb-6 leading-relaxed font-medium"></p>
      <div class="flex justify-end">
        <button type="button" onclick="closeAlertModal()" class="px-5 py-2.5 rounded-xl text-sm font-bold bg-[#0f294a] text-white hover:bg-blue-900 transition">
          Entendido
        </button>
      </div>
    </div>
  </div>

  <!-- Modal de Confirmación de Entrega -->
  <div id="confirm-modal" class="fixed inset-0 bg-slate-900/75 backdrop-blur-sm z-50 hidden items-center justify-center p-4 no-print">
    <div class="bg-white rounded-2xl max-w-md w-full p-6 shadow-2xl border border-slate-200">
      <div class="flex items-center gap-3 text-[#0f294a] mb-3">
        <div class="w-10 h-10 rounded-full bg-amber-100 text-amber-600 flex items-center justify-center shrink-0">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
          </svg>
        </div>
        <h3 id="confirm-modal-title" class="text-lg font-bold">Confirmar Entrega Grupal</h3>
      </div>
      <p id="confirm-modal-message" class="text-sm text-slate-600 mb-6 leading-relaxed"></p>
      <div class="flex justify-end gap-3">
        <button type="button" onclick="closeConfirmModal()" class="px-4 py-2 rounded-xl text-sm font-medium text-slate-600 hover:bg-slate-100 transition">
          Cancelar
        </button>
        <button type="button" id="confirm-modal-btn" class="px-5 py-2 rounded-xl text-sm font-bold bg-emerald-600 text-white hover:bg-emerald-700 transition">
          Finalizar y Entregar
        </button>
      </div>
    </div>
  </div>

  <!-- Modal Configuración EmailJS (Para el Docente) -->
  <div id="emailjs-modal" class="fixed inset-0 bg-slate-900/75 backdrop-blur-sm z-50 hidden items-center justify-center p-4 no-print">
    <div class="bg-white rounded-2xl max-w-md w-full p-6 shadow-2xl border border-slate-200">
      <div class="flex items-center justify-between border-b border-slate-200 pb-3 mb-4">
        <h3 class="text-base font-extrabold text-[#0f294a]">Configuración de Correo Docente (EmailJS)</h3>
        <button type="button" onclick="closeEmailConfig()" class="text-slate-400 hover:text-slate-700 text-xl leading-none">&times;</button>
      </div>
      <p class="text-xs text-slate-600 mb-4 leading-relaxed">
        Configure sus credenciales gratuitas de <strong>EmailJS</strong> para que al finalizar cada grupo, las respuestas, integrantes, auditoría y esquemas 3FN lleguen directo a su correo.
      </p>
      <div class="space-y-3 text-xs">
        <div>
          <label class="block font-semibold text-slate-700 mb-1">Public Key:</label>
          <input type="text" id="cfg_public_key" placeholder="Ej. user_XXXXXXXXXXXX"
            class="w-full px-3 py-2 border border-slate-300 rounded-xl font-mono focus:ring-2 focus:ring-blue-600 outline-none" />
        </div>
        <div>
          <label class="block font-semibold text-slate-700 mb-1">Service ID:</label>
          <input type="text" id="cfg_service_id" placeholder="Ej. service_xxxxxxx"
            class="w-full px-3 py-2 border border-slate-300 rounded-xl font-mono focus:ring-2 focus:ring-blue-600 outline-none" />
        </div>
        <div>
          <label class="block font-semibold text-slate-700 mb-1">Template ID:</label>
          <input type="text" id="cfg_template_id" placeholder="Ej. template_xxxxxxx"
            class="w-full px-3 py-2 border border-slate-300 rounded-xl font-mono focus:ring-2 focus:ring-blue-600 outline-none" />
        </div>
        <div>
          <label class="block font-semibold text-slate-700 mb-1">Correo del Docente (Destinatario):</label>
          <input type="email" id="cfg_teacher_email" placeholder="cesar.rengifo@ejemplo.com"
            class="w-full px-3 py-2 border border-slate-300 rounded-xl focus:ring-2 focus:ring-blue-600 outline-none" />
        </div>
      </div>
      <div class="flex justify-end gap-2 mt-6">
        <button type="button" onclick="closeEmailConfig()" class="px-4 py-2 rounded-xl text-xs font-semibold text-slate-600 hover:bg-slate-100">Cerrar</button>
        <button type="button" onclick="saveEmailConfig()" class="px-4 py-2 rounded-xl text-xs font-bold bg-[#0f294a] text-white hover:bg-blue-900">Guardar</button>
      </div>
    </div>
  </div>

  <!-- ===================================================================== -->
  <!-- PANTALLA 1: LOBBY COLABORATIVO (CREAR SALA VS UNIRSE A SALA)          -->
  <!-- ===================================================================== -->
  <div id="lobby-screen" class="max-w-5xl mx-auto w-full px-4 sm:px-6 py-8 flex-1">
    <div class="bg-white rounded-2xl shadow-md border border-slate-200 overflow-hidden">
      <!-- Membrete Oficial UNEFA -->
      <div class="bg-[#0f294a] text-white p-6 sm:p-8 text-center relative">
        <button type="button" onclick="openEmailConfig()" title="Configurar envío de correo EmailJS"
          class="absolute top-4 right-4 text-xs bg-white/10 hover:bg-white/20 text-amber-300 px-3 py-1.5 rounded-xl border border-white/15 transition">
          ⚙ Correo Docente
        </button>

        <div class="inline-flex items-center justify-center w-14 h-14 rounded-2xl bg-amber-500/20 border border-amber-400/40 text-amber-400 mb-3">
          <svg class="w-8 h-8" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 14l9-5-9-5-9 5 9 5z" />
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z" />
          </svg>
        </div>

        <p class="text-[11px] sm:text-xs font-bold uppercase tracking-widest text-amber-300">
          República Bolivariana de Venezuela • Ministerio del Poder Popular para la Defensa
        </p>
        <h1 class="text-lg sm:text-2xl font-extrabold mt-1">
          Universidad Nacional Experimental Politécnica de la Fuerza Armada Bolivariana (UNEFA)
        </h1>
        <p class="text-xs sm:text-sm text-slate-300 font-semibold mt-1">
          NÚCLEO GUÁRICO — SEDE TUCUPIDO
        </p>

        <!-- Ficha Académica Oficial del Taller -->
        <div class="mt-6 grid grid-cols-2 sm:grid-cols-4 gap-2 text-left bg-slate-900/60 p-4 rounded-xl border border-slate-700 text-xs">
          <div>
            <span class="text-slate-400 block">Departamento:</span>
            <strong class="text-white">ING. DE SISTEMAS</strong>
          </div>
          <div>
            <span class="text-slate-400 block">Asignatura:</span>
            <strong class="text-white">DISEÑO DE SISTEMAS</strong>
          </div>
          <div>
            <span class="text-slate-400 block">Semestre / Sección:</span>
            <strong class="text-amber-300">6° Sem. • 06S-2633</strong>
          </div>
          <div>
            <span class="text-slate-400 block">Fecha / Ponderación:</span>
            <strong class="text-emerald-300">19/11/2026 • 10% (20 Pts)</strong>
          </div>
          <div class="col-span-2 sm:col-span-4 border-t border-slate-700/80 pt-2 mt-1 flex flex-wrap justify-between gap-2">
            <span><span class="text-slate-400">Evaluación:</span> <strong class="text-white">TALLER N° 1 (Unidad 3 — Colaborativo Multi-Dispositivo)</strong></span>
            <span><span class="text-slate-400">Docente:</span> <strong class="text-amber-300">CESAR E. RENGIFO S.</strong></span>
          </div>
        </div>
      </div>

      <div class="p-6 sm:p-8 space-y-6">
        <!-- Reglas de Cupo por Dispositivo y Anti-Abandono -->
        <div class="bg-amber-50 border-l-4 border-amber-500 p-4 rounded-r-xl text-xs sm:text-sm text-slate-700 space-y-1.5">
          <h2 class="font-extrabold text-[#0f294a] uppercase text-xs tracking-wider">Normas de Control de Dispositivos y Seguridad (90 Minutos):</h2>
          <ul class="list-disc list-inside space-y-1">
            <li><strong>Control estricto de cupos por grupo:</strong> Si el grupo es de <strong>2 integrantes</strong>, el sistema permitirá conectar <u>máximo 2 dispositivos</u>. Si es de <strong>3 integrantes</strong>, permitirá conectar <u>máximo 3 dispositivos</u>.</li>
            <li><strong>Bloqueo Anti-Salida de Pantalla:</strong> Al ingresar al examen se activará Pantalla Completa. Si <strong>cualquiera</strong> de los dispositivos del grupo sale de pantalla completa, cambia de pestaña o minimiza la ventana, <u>la prueba terminará inmediatamente para todo el grupo</u>.</li>
          </ul>
        </div>

        <!-- Selector de Modo: Crear Sala vs Unirse a Sala -->
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
          <!-- OPCIÓN A: CREAR SALA DE GRUPO (LÍDER / INTEGRANTE 1) -->
          <div class="p-5 sm:p-6 rounded-2xl bg-slate-50 border-2 border-[#0f294a]/20 flex flex-col justify-between">
            <div>
              <div class="flex items-center gap-2 mb-3">
                <span class="w-7 h-7 rounded-lg bg-[#0f294a] text-white font-bold text-xs flex items-center justify-center">A</span>
                <h3 class="text-base font-extrabold text-[#0f294a]">Crear Nueva Sala de Grupo</h3>
              </div>
              <p class="text-xs text-slate-600 mb-4">
                El <strong>Integrante N° 1</strong> define el tamaño exacto del grupo y genera el código de acceso para sus compañeros.
              </p>

              <!-- Selector Obligatorio de Tamaño de Grupo (2 vs 3) -->
              <div class="mb-4">
                <label class="block text-xs font-bold text-[#0f294a] mb-2">1. Seleccione el Tamaño del Grupo (Límite de Dispositivos) *</label>
                <div class="grid grid-cols-2 gap-2.5">
                  <label id="lbl-size-2" onclick="selectGroupSize(2)"
                    class="cursor-pointer p-3 rounded-xl border-2 border-[#0f294a] bg-blue-50 text-center transition">
                    <input type="radio" name="group_size" value="2" checked class="sr-only" />
                    <span class="block text-sm font-extrabold text-[#0f294a]">2 Integrantes</span>
                    <span class="block text-[11px] font-semibold text-blue-700 mt-0.5">Máximo 2 dispositivos</span>
                  </label>
                  <label id="lbl-size-3" onclick="selectGroupSize(3)"
                    class="cursor-pointer p-3 rounded-xl border-2 border-slate-200 bg-white text-center hover:border-blue-400 transition">
                    <input type="radio" name="group_size" value="3" class="sr-only" />
                    <span class="block text-sm font-extrabold text-[#0f294a]">3 Integrantes</span>
                    <span class="block text-[11px] font-semibold text-slate-500 mt-0.5">Máximo 3 dispositivos</span>
                  </label>
                </div>
              </div>

              <!-- Datos del Integrante 1 -->
              <div class="space-y-3 mb-5">
                <div>
                  <label class="block text-xs font-semibold text-slate-700 mb-1">Apellidos y Nombres (Integrante 1) *</label>
                  <input type="text" id="create_name" placeholder="Ej. Pérez Rodríguez, Carlos"
                    class="w-full px-3.5 py-2 bg-white border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-blue-600 outline-none" />
                </div>
                <div>
                  <label class="block text-xs font-semibold text-slate-700 mb-1">Cédula de Identidad *</label>
                  <input type="text" id="create_ci" placeholder="Ej. V-28.456.789"
                    class="w-full px-3.5 py-2 bg-white border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-blue-600 outline-none" />
                </div>
              </div>
            </div>

            <button type="button" id="btn-create-room" onclick="createCollaborativeRoom()"
              class="w-full py-3 px-5 rounded-xl text-sm font-extrabold bg-[#0f294a] hover:bg-blue-900 text-white shadow-md transition flex items-center justify-center gap-2">
              <svg class="w-4 h-4 text-amber-400" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M12 4v16m8-8H4" />
              </svg>
              Crear Sala e Iniciar Prueba
            </button>
          </div>

          <!-- OPCIÓN B: UNIRSE A SALA EXISTENTE (INTEGRANTE 2 O 3) -->
          <div class="p-5 sm:p-6 rounded-2xl bg-slate-50 border-2 border-emerald-600/25 flex flex-col justify-between">
            <div>
              <div class="flex items-center gap-2 mb-3">
                <span class="w-7 h-7 rounded-lg bg-emerald-600 text-white font-bold text-xs flex items-center justify-center">B</span>
                <h3 class="text-base font-extrabold text-[#0f294a]">Unirse a Sala Existente</h3>
              </div>
              <p class="text-xs text-slate-600 mb-4">
                Si su compañero ya creó la sala del grupo, ingrese el <strong>Código de Sala</strong> y sus datos personales para colaborar desde este dispositivo.
              </p>

              <div class="space-y-3 mb-5">
                <div>
                  <label class="block text-xs font-bold text-emerald-800 mb-1">Código de Sala Compartido (6 caracteres) *</label>
                  <input type="text" id="join_code" maxlength="6" placeholder="Ej. A7K9P2"
                    class="w-full px-3.5 py-2.5 bg-white border-2 border-emerald-500/50 rounded-xl text-base font-mono font-extrabold uppercase tracking-widest text-center text-[#0f294a] focus:ring-2 focus:ring-emerald-600 outline-none" />
                </div>
                <div>
                  <label class="block text-xs font-semibold text-slate-700 mb-1">Apellidos y Nombres (Su identificación) *</label>
                  <input type="text" id="join_name" placeholder="Ej. Gómez Silva, María"
                    class="w-full px-3.5 py-2 bg-white border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-emerald-600 outline-none" />
                </div>
                <div>
                  <label class="block text-xs font-semibold text-slate-700 mb-1">Cédula de Identidad *</label>
                  <input type="text" id="join_ci" placeholder="Ej. V-29.123.456"
                    class="w-full px-3.5 py-2 bg-white border border-slate-300 rounded-xl text-sm focus:ring-2 focus:ring-emerald-600 outline-none" />
                </div>
              </div>
            </div>

            <button type="button" id="btn-join-room" onclick="joinCollaborativeRoom()"
              class="w-full py-3 px-5 rounded-xl text-sm font-extrabold bg-emerald-600 hover:bg-emerald-700 text-white shadow-md transition flex items-center justify-center gap-2">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M11 16l-4-4m0 0l4-4m-4 4h14m-5 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h7a3 3 0 013 3v1" />
              </svg>
              Conectar Dispositivo a la Sala
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ===================================================================== -->
  <!-- PANTALLA 2: ENTORNO COLABORATIVO DE EVALUACIÓN (SINCRONIZADO)         -->
  <!-- ===================================================================== -->
  <div id="active-exam-screen" class="hidden flex-1 flex flex-col">

    <!-- Barra Superior Fija con Código de Sala, Cupo de Dispositivos y Temporizador -->
    <header class="bg-[#0f294a] text-white shadow-md sticky top-0 z-40 no-print">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 py-2.5 flex flex-wrap items-center justify-between gap-3">
        <!-- Código de Sala y Cupo -->
        <div class="flex flex-wrap items-center gap-2.5">
          <div class="bg-amber-500/20 border border-amber-400/50 px-3 py-1 rounded-xl">
            <span class="text-[10px] uppercase tracking-wider text-amber-300 block font-bold">Código de Sala</span>
            <span id="header-room-code" class="font-mono text-sm sm:text-base font-extrabold text-white tracking-widest">------</span>
          </div>

          <div class="bg-slate-800/90 border border-slate-600 px-3 py-1 rounded-xl">
            <span class="text-[10px] uppercase tracking-wider text-slate-300 block font-bold">Cupo de Dispositivos</span>
            <span id="header-device-quota" class="text-xs sm:text-sm font-extrabold text-emerald-400">1 / 2 conectados</span>
          </div>

        
