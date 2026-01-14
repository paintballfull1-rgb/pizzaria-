# pizzaria-<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Cabeleireiro Sr. Roberto</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f1216;
      --card:#151a21;
      --muted:#8a94a6;
      --text:#e9edf3;
      --primary:#3ab0ff;
      --primary-2:#2a8bd1;
      --accent:#7cf29a;
      --danger:#ff6b6b;
      --shadow:0 10px 30px rgba(0,0,0,.35);
      --radius:14px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;
      background:linear-gradient(120deg,#0b0e12 0%, #12161d 60%, #0f1216 100%);
      color:var(--text);
    }
    a{color:var(--primary);text-decoration:none}
    header{
      position:sticky;top:0;z-index:50;
      backdrop-filter:saturate(1.2) blur(8px);
      background:rgba(15,18,22,.7);
      border-bottom:1px solid rgba(255,255,255,.06);
    }
    .nav{
      max-width:1100px;margin:0 auto;padding:14px 20px;
      display:flex;align-items:center;gap:16px;justify-content:space-between;
    }
    .brand{
      display:flex;align-items:center;gap:12px;font-weight:700;letter-spacing:.2px;
    }
    .brand .logo{
      width:38px;height:38px;border-radius:10px;
      background:linear-gradient(135deg,var(--primary),var(--accent));
      box-shadow:0 6px 18px rgba(58,176,255,.35);
    }
    .nav-links{display:flex;gap:18px;flex-wrap:wrap}
    .nav-links a{
      padding:8px 12px;border-radius:10px;color:var(--text);
    }
    .nav-links a:hover{background:rgba(255,255,255,.06)}
    .cta{
      padding:10px 14px;border-radius:12px;background:var(--primary);color:#06121a;font-weight:700;
      box-shadow:0 8px 20px rgba(58,176,255,.35);
    }
    .cta:hover{background:var(--primary-2)}
    .hero{
      max-width:1100px;margin:24px auto;padding:24px 20px;
      display:grid;grid-template-columns:1.2fr .8fr;gap:24px;
    }
    .card{
      background:var(--card);border:1px solid rgba(255,255,255,.06);
      border-radius:var(--radius);box-shadow:var(--shadow);
    }
    .hero .intro{
      padding:28px;
      background:
        radial-gradient(1200px 400px at 10% -10%, rgba(58,176,255,.15), transparent 40%),
        radial-gradient(800px 300px at 90% 120%, rgba(124,242,154,.12), transparent 40%),
        var(--card);
    }
    .intro h1{margin:0 0 10px;font-size:2rem}
    .intro p{color:var(--muted);margin:0 0 18px}
    .badges{display:flex;gap:10px;flex-wrap:wrap;margin:12px 0 18px}
    .badge{
      padding:8px 12px;border-radius:999px;background:rgba(255,255,255,.06);
      border:1px solid rgba(255,255,255,.08);color:#cfe7ff;font-weight:600;font-size:.9rem;
    }
    .highlight{
      display:flex;gap:14px;align-items:center;margin-top:8px;color:#cfe7ff;
    }
    .highlight .dot{
      width:10px;height:10px;border-radius:50%;
      background:linear-gradient(135deg,var(--accent),#4bdc7f);
      box-shadow:0 0 12px rgba(124,242,154,.6);
    }
    .hero .photo{
      position:relative;overflow:hidden;
      background:linear-gradient(135deg,#10151b,#0c1116);
    }
    .photo img{
      width:100%;height:100%;object-fit:cover;opacity:.9;filter:saturate(1.05) contrast(1.05);
    }
    .section{max-width:1100px;margin:0 auto;padding:8px 20px 28px}
    .section h2{margin:18px 0 14px}
    .grid{
      display:grid;grid-template-columns:repeat(3,1fr);gap:18px;
    }
    .service, .gallery-item, .contact-card, .schedule-card{
      padding:18px;border-radius:var(--radius);background:var(--card);
      border:1px solid rgba(255,255,255,.06);box-shadow:var(--shadow);
    }
    .service h3{margin:0 0 6px}
    .price{color:var(--accent);font-weight:700}
    .muted{color:var(--muted)}
    .schedule-card form{display:grid;gap:12px}
    input, select, textarea{
      width:100%;padding:12px;border-radius:12px;border:1px solid rgba(255,255,255,.08);
      background:#0e1318;color:var(--text);
    }
    input::placeholder, textarea::placeholder{color:#7a8596}
    .btn{
      padding:12px 14px;border:none;border-radius:12px;background:var(--primary);color:#06121a;font-weight:700;
      cursor:pointer;box-shadow:0 8px 20px rgba(58,176,255,.35);
    }
    .btn:hover{background:var(--primary-2)}
    .btn-outline{
      background:transparent;color:var(--text);border:1px solid rgba(255,255,255,.14);
    }
    .appointments{
      margin-top:12px;border-top:1px dashed rgba(255,255,255,.12);padding-top:12px;
    }
    .appt{
      display:flex;justify-content:space-between;align-items:center;padding:10px;border-radius:10px;
      background:rgba(255,255,255,.04);margin-bottom:8px;
    }
    .appt small{color:var(--muted)}
    .danger{color:var(--danger)}
    .gallery{
      display:grid;grid-template-columns:repeat(4,1fr);gap:12px;
    }
    .gallery-item{padding:0;overflow:hidden}
    .gallery-item img{width:100%;height:180px;object-fit:cover;display:block}
    .contact-grid{display:grid;grid-template-columns:1.2fr .8fr;gap:18px}
    iframe{border:0;border-radius:12px;width:100%;height:280px}
    footer{
      margin-top:24px;padding:24px 20px;border-top:1px solid rgba(255,255,255,.06);
      background:rgba(15,18,22,.6);text-align:center;color:var(--muted)
    }
    /* Responsivo */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr}
      .grid{grid-template-columns:1fr 1fr}
      .gallery{grid-template-columns:1fr 1fr 1fr}
      .contact-grid{grid-template-columns:1fr}
    }
    @media (max-width:640px){
      .nav{flex-wrap:wrap}
      .grid{grid-template-columns:1fr}
      .gallery{grid-template-columns:1fr 1fr}
      .hero{padding:16px}
      .section{padding:8px 16px 24px}
    }
  </style>
</head>
<body>
  <header>
    <div class="nav">
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <div>
          <div style="font-size:1.05rem">Cabeleireiro Sr. Roberto</div>
          <small class="muted">Borda da Mata • MG</small>
        </div>
      </div>
      <nav class="nav-links">
        <a href="#servicos">Serviços</a>
        <a href="#agendamento">Agendamento</a>
        <a href="#galeria">Galeria</a>
        <a href="#contato">Contato</a>
      </nav>
      <a class="cta" href="#agendamento">Agendar agora</a>
    </div>
  </header>

  <section class="hero">
    <div class="card intro">
      <h1>Estilo, precisão e cuidado</h1>
      <p>Atendimento profissional com horário marcado, cortes clássicos e modernos, barba e tratamentos capilares. Experiência pensada para você.</p>
      <div class="badges">
        <span class="badge">Cortes masculinos</span>
        <span class="badge">Barba e acabamento</span>
        <span class="badge">Coloração</span>
        <span class="badge">Hidratação</span>
      </div>
      <div class="highlight">
        <span class="dot"></span>
        <span>Agenda aberta de segunda a sábado — reserve seu horário.</span>
      </div>
    </div>
    <div class="card photo">
      <img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?q=80&w=1200&auto=format&fit=crop" alt="Barbearia moderna">
    </div>
  </section>

  <section id="servicos" class="section">
    <h2>Serviços oferecidos</h2>
    <div class="grid">
      <div class="service">
        <h3>Corte masculino</h3>
        <p class="muted">Tesoura e máquina, finalização com produto.</p>
        <div class="price">R$ 45</div>
      </div>
      <div class="service">
        <h3>Barba completa</h3>
        <p class="muted">Modelagem, toalha quente e acabamento.</p>
        <div class="price">R$ 35</div>
      </div>
      <div class="service">
        <h3>Corte + Barba</h3>
        <p class="muted">Pacote completo com desconto.</p>
        <div class="price">R$ 70</div>
      </div>
      <div class="service">
        <h3>Coloração</h3>
        <p class="muted">Cobertura de fios brancos e tonalização.</p>
        <div class="price">R$ 60</div>
      </div>
      <div class="service">
        <h3>Hidratação</h3>
        <p class="muted">Tratamento para saúde dos fios.</p>
        <div class="price">R$ 50</div>
      </div>
      <div class="service">
        <h3>Sobrancelha</h3>
        <p class="muted">Design e acabamento.</p>
        <div class="price">R$ 25</div>
      </div>
    </div>
  </section>

  <section id="agendamento" class="section">
    <h2>Agendamento de horários</h2>
    <div class="schedule-card">
      <form id="form-agenda">
        <div class="grid">
          <div>
            <label for="nome">Nome completo</label>
            <input id="nome" name="nome" type="text" placeholder="Seu nome" required />
          </div>
          <div>
            <label for="telefone">Telefone (WhatsApp)</label>
            <input id="telefone" name="telefone" type="tel" placeholder="(xx) xxxxx-xxxx" required />
          </div>
          <div>
            <label for="servico">Serviço</label>
            <select id="servico" name="servico" required>
              <option value="">Selecione</option>
              <option>Corte masculino</option>
              <option>Barba completa</option>
              <option>Corte + Barba</option>
              <option>Coloração</option>
              <option>Hidratação</option>
              <option>Sobrancelha</option>
            </select>
          </div>
          <div>
            <label for="data">Data</label>
            <input id="data" name="data" type="date" required />
          </div>
          <div>
            <label for="hora">Hora</label>
            <select id="hora" name="hora" required>
              <!-- Horários gerados via JS -->
            </select>
          </div>
        </div>
        <div>
          <label for="obs">Observações</label>
          <textarea id="obs" name="obs" rows="3" placeholder="Preferências, referências de corte..."></textarea>
        </div>
        <div style="display:flex;gap:10px;flex-wrap:wrap">
          <button class="btn" type="submit">Reservar horário</button>
          <button class="btn btn-outline" type="button" id="btn-exportar">Exportar agenda (CSV)</button>
        </div>
      </form>

      <div class="appointments" id="lista-agendamentos">
        <!-- Lista de agendamentos -->
      </div>
    </div>
  </section>

  <section id="galeria" class="section">
    <h2>Galeria de cortes</h2>
    <div class="gallery">
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1511367461989-f85a21fda167?q=80&w=1200&auto=format&fit=crop" alt="Corte 1"></div>
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?q=80&w=1200&auto=format&fit=crop" alt="Corte 2"></div>
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1519415943484-9fa18778a0e5?q=80&w=1200&auto=format&fit=crop" alt="Corte 3"></div>
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=1200&auto=format&fit=crop" alt="Corte 4"></div>
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1517832207067-4db24a2ae47c?q=80&w=1200&auto=format&fit=crop" alt="Corte 5"></div>
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1516979187457-637abb4f9353?q=80&w=1200&auto=format&fit=crop" alt="Corte 6"></div>
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1512496015851-a90fb38ba796?q=80&w=1200&auto=format&fit=crop" alt="Corte 7"></div>
      <div class="gallery-item"><img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?q=80&w=1200&auto=format&fit=crop" alt="Corte 8"></div>
    </div>
  </section>

  <section id="contato" class="section">
    <h2>Contato e localização</h2>
    <div class="contact-grid">
      <div class="contact-card">
        <h3>Fale com o Sr. Roberto</h3>
        <p><strong>Telefone:</strong> (35) 9 9999-9999</p>
        <p><strong>Endereço:</strong> Rua Central, 123 — Borda da Mata, MG</p>
        <p><strong>Horário:</strong> Seg–Sex 9h–19h • Sáb 9h–16h</p>
        <div style="display:flex;gap:10px;margin-top:10px;flex-wrap:wrap">
          <a class="btn" href="https://wa.me/5535999999999" target="_blank" rel="noopener">WhatsApp</a>
          <a class="btn btn-outline" href="tel:+5535999999999">Ligar</a>
        </div>
      </div>
      <div class="contact-card">
        <h3>Mapa</h3>
        <iframe
          src="https://www.google.com/maps?q=Borda%20da%20Mata%2C%20MG&output=embed"
          allowfullscreen
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
    </div>
  </section>

  <footer>
    © <span id="ano"></span> Cabeleireiro Sr. Roberto — Todos os direitos reservados.
  </footer>

  <script>
    // Utilidades
    const $ = (sel, ctx=document) => ctx.querySelector(sel);
    const $$ = (sel, ctx=document) => Array.from(ctx.querySelectorAll(sel));

    // Inicializa ano
    $('#ano').textContent = new Date().getFullYear();

    // Gera horários (09:00–19:00, a cada 30 min)
    function gerarHorarios(){
      const select = $('#hora');
      select.innerHTML = '';
      const inicio = 9, fim = 19;
      for(let h=inicio; h<=fim; h++){
        for(let m of [0,30]){
          const label = `${String(h).padStart(2,'0')}:${String(m).padStart(2,'0')}`;
          const opt = document.createElement('option');
          opt.value = label; opt.textContent = label;
          select.appendChild(opt);
        }
      }
    }
    gerarHorarios();

    // Valida data mínima (hoje)
    const hojeISO = new Date().toISOString().split('T')[0];
    $('#data').setAttribute('min', hojeISO);

    // LocalStorage
    const STORAGE_KEY = 'sr_roberto_agendamentos';
    function getAgendamentos(){
      try { return JSON.parse(localStorage.getItem(STORAGE_KEY)) || []; }
      catch { return []; }
    }
    function setAgendamentos(lista){
      localStorage.setItem(STORAGE_KEY, JSON.stringify(lista));
    }

    // Renderiza lista
    function renderAgendamentos(){
      const cont = $('#lista-agendamentos');
      const lista = getAgendamentos().sort((a,b)=>{
        const da = new Date(`${a.data}T${a.hora}:00`);
        const db = new Date(`${b.data}T${b.hora}:00`);
        return da - db;
      });
      if(!lista.length){
        cont.innerHTML = '<p class="muted">Nenhum horário reservado ainda.</p>';
        return;
      }
      cont.innerHTML = '';
      lista.forEach((item, idx)=>{
        const div = document.createElement('div');
        div.className = 'appt';
        div.innerHTML = `
          <div>
            <strong>${item.nome}</strong> • <small>${item.telefone}</small><br>
            <small>${item.servico} — ${item.data} às ${item.hora}</small>
            ${item.obs ? `<br><small class="muted">Obs: ${item.obs}</small>` : ''}
          </div>
          <button class="btn btn-outline" data-del="${idx}">Cancelar</button>
        `;
        cont.appendChild(div);
      });
      // Bind cancelar
      $$('#lista-agendamentos button[data-del]').forEach(btn=>{
        btn.addEventListener('click', (e)=>{
          const idx = Number(e.currentTarget.dataset.del);
          const lista = getAgendamentos();
          const appt = lista[idx];
          if(confirm(`Cancelar ${appt.servico} de ${appt.nome} em ${appt.data} às ${appt.hora}?`)){
            lista.splice(idx,1);
            setAgendamentos(lista);
            renderAgendamentos();
          }
        });
      });
    }
    renderAgendamentos();

    // Verifica conflito de horário
    function existeConflito(data, hora){
      return getAgendamentos().some(a => a.data === data && a.hora === hora);
    }

    // Submissão do formulário
    $('#form-agenda').addEventListener('submit', (e)=>{
      e.preventDefault();
      const nome = $('#nome').value.trim();
      const telefone = $('#telefone').value.trim();
      const servico = $('#servico').value;
      const data = $('#data').value;
      const hora = $('#hora').value;
      const obs = $('#obs').value.trim();

      if(!nome || !telefone || !servico || !data || !hora){
        alert('Preencha todos os campos obrigatórios.');
        return;
      }
      if(existeConflito(data, hora)){
        alert('Este horário já está reservado. Escolha outro.');
        return;
      }
      const novo = {nome, telefone, servico, data, hora, obs};
      const lista = getAgendamentos();
      lista.push(novo);
      setAgendamentos(lista);
      renderAgendamentos();
      e.target.reset();
      gerarHorarios(); // mantém select
      alert('Horário reservado com sucesso!');
    });

    // Exportar CSV
    $('#btn-exportar').addEventListener('click', ()=>{
      const lista = getAgendamentos();
      if(!lista.length){ alert('Nenhum agendamento para exportar.'); return; }
      const header = ['Nome','Telefone','Serviço','Data','Hora','Observações'];
      const linhas = [header.join(',')].concat(
        lista.map(a => [
          `"${a.nome}"`,
          `"${a.telefone}"`,
          `"${a.servico}"`,
          a.data,
          a.hora,
          `"${(a.obs||'').replace(/"/g,'""')}"`,
        ].join(','))
      );
      const blob = new Blob([linhas.join('\n')], {type:'text/csv;charset=utf-8;'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download = 'agenda_sr_roberto.csv';
      document.body.appendChild(a); a.click(); a.remove();
      URL.revokeObjectURL(url);
    });
  </script>
</body>
</html>
