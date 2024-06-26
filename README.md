![banner](banner.png)
# Proyecto 3: Landing de Negocio
## Planteamiento
En esta demo, generaremos una tiendaa de articulos de mascotas. La idea principal es de inmediato entregar el objeto de la página, siguiente a esto mostrar imagenes llamativas que potencian la principal idea ademas de mostrar informacion de ofertas y/o el espiritu de la empresa. Lo proximo entregar el catalogo de productos y por último un medio de contacto y solicitud de pedidos especiales a partir de un formulario básico.
## Requerimientos
- El sitio debe incluir las estructuras de `Header`, `Main`, `Aside`, `Products`, `Form`, `Footer`.
- El sitio debe mostar diferentes etiquetas, estableciendo los estándares de HTML5 para dar mayor semántica
## Esquema de pagina
![Esquema de la pagina](esquemaPagina.jpg)
## Solucion General
1. Tenemnos primero el `Header`, con el nombre de la empresa +Cotitas, direcciones que ayudan a avanzar  mas rápido en la pagina y en el borde derecho un buscador.
   ```ruby
    <header>
        <div class="logo">
            <img src="https://cdn-icons-png.flaticon.com/512/30/30658.png" alt="Logo de la tienda">
            <h1>COTITAS</h1>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Inicio</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#contact">Contacto</a></li>
            </ul>
            <form class="buscador">
                <input type="text" placeholder="Buscar productos...">
                <button type="submit"><i class="fas fa-search"></i></button>
            </form>
        </nav>
    </header>
   ```
2. Siguiente a esto el `Main` contiene una pequeña presentación de la empresa, un aside con la class `galeria`, despues la seccion de productos y por ultimo un `form`(Formulario).
   ```ruby
    <main>
        <section id="home">
            <h2>Bienvenido a +Cotitas</h2>
            <p>Tu tienda favorita de artículos para mascotas.</p>
        </section>
        <section class="galeria">
            <div class="galeria-container">
                <div class="galeria-slide">
                    <img src="https://www.zooplus.es/magazine/wp-content/uploads/2020/01/Escuela-para-cachorros-768x512.jpeg" alt="Perritos jugando">
                    <div class="galeria-caption">Productos para cachorros en descuento</div>
                </div>
                <div class="galeria-slide">
                    <img src="https://imagenes.20minutos.es/files/image_1920_1080/uploads/imagenes/2023/07/14/un-gato-durmiendo-de-lado.jpeg" alt="Gato durmiendo">
                    <div class="galeria-caption">La primera compra con envío gratis</div>
                </div>
                <div class="galeria-slide">
                    <img src="https://contigoentucasa.com/wp-content/uploads/2022/01/0000_Cuidado-de-animales-de-compania.jpg" alt="Alimento para mascotas">
                    <div class="galeria-caption">El cuidado de tu mascota nos importa</div>
                </div>
            </div>
        </section>
        <section id="productos" class="seccion-productos">
            <h2>Nuestros productos</h2>
            <div class="producto-grid">
                <div class="producto">
                    <div class="producto-info">
                        <h3>Collar para perros</h3>
                        <p>Precio: $5990</p>
                        <button class="boton-carrito" class="fas fa-shopping-cart"></i>Agregar</button>
                    </div>
                    <img src="https://cdn11.bigcommerce.com/s-d331r3r4ex/images/stencil/1280x1280/products/22078/44800/__1707__76442.1691700576.jpg?c=1?imbypass=on" alt="Collar para perros">
                </div>
                <div class="producto">
                    <div class="producto-info">
                        <h3>Juguete para gatos</h3>
                        <p>Precio: $4990</p>
                        <button class="boton-carrito" class="fas fa-shopping-cart"></i>Agregar</button>
                    </div>
                    <img src="https://puppieshouse.cl/857-large_default/juguete-varita-para-gatos-.jpg" alt="Juguete para gatos">
                </div>
                <div class="producto">
                    <div class="producto-info">
                        <h3>Estructura para Gatos</h3>
                        <p>Precio: $45900</p>
                        <button class="boton-carrito" class="fas fa-shopping-cart"></i>Agregar</button>
                    </div>
                    <img src="https://s.libertaddigital.com/2021/02/01/feandrea-arbol-para-gatos.jpg" alt="Estructura para gatos">
                </div>
                <div class="producto">
                    <div class="producto-info">
                        <h3>Hueso para perro</h3>
                        <p>Precio: $3990</p>
                        <button class="boton-carrito" class="fas fa-shopping-cart"></i>Agregar</button>
                    </div>
                    <img src="https://elarcapet.cl/webapp/wp-content/uploads/2020/09/HUESOS-PARA-PERROS.jpg" alt="Hueso para perro">
                </div>
                <div class="producto">
                    <div class="producto-info">
                        <h3>Pocillo para perro</h3>
                        <p>Precio: $4490</p>
                        <button class="boton-carrito" class="fas fa-shopping-cart"></i>Agregar</button>
                    </div>
                    <img src="https://i.etsystatic.com/12566574/r/il/c5777f/1780105818/il_fullxfull.1780105818_hfkv.jpg" alt="Pocillo para perro">
                </div>
                <div class="producto">
                    <div class="producto-info">
                        <h3>Bebedero para Gatos</h3>
                        <p>Precio: $7990</p>
                        <button class="boton-carrito">Agregar</button>
                    </div>
                    <img src="https://cdnx.jumpseller.com/cody-store/image/32662340/resize/640/500?1677630372" alt="Bebedero para Gatos">
                </div>
            </div>
        </section>

        <section id="contact">
            <h2>Contacto</h2>
            <form action="#">
                <label for="name">Nombre:</label>
                <input type="text" id="name" name="name" required>
                
                <label for="email">Correo Electrónico:</label>
                <input type="email" id="email" name="email" required>
                
                <label for="message">Mensaje:</label>
                <textarea id="message" name="message" required></textarea>
                
                <button type="submit">Enviar</button>
            </form>
            <br>
            <br>
            <br>
        </section>
    </main>
   ```

3. Por ultimo el `footer` contiene los derechos reservados, informacion y contacto de la empresa.
      ```ruby
      <footer>
        <ul class="footer-links">
            <li><a href="#terminosYCondiciones">Términos y Condiciones</a></li>
            <li><a href="https://youtu.be/dQw4w9WgXcQ" target="_blank">Instagram</a></li>
            <li><a href="#home">Inicio</a></li>
        </ul>
        <p>&copy; 2024 +Cotitas. Todos los derechos reservados.</p>

       </footer>
      ```

      
