<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jason Katz - Academic Website</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            color: #333;
            background-color: #fdfdfd;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            color: white;
            padding: 40px 0;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-content h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            font-weight: 300;
        }

        .header-content p {
            font-size: 1.2em;
            opacity: 0.9;
            margin-bottom: 20px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .contact-info a {
            color: white;
            text-decoration: none;
            padding: 8px 16px;
            border: 1px solid rgba(255,255,255,0.3);
            border-radius: 20px;
            transition: all 0.3s ease;
        }

        .contact-info a:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }

        /* Navigation */
        nav {
            background: #34495e;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .nav-links {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 30px;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 5px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .nav-links a:hover, .nav-links a.active {
            background: #3498db;
            transform: translateY(-2px);
        }

        /* Main Content */
        main {
            padding: 40px 0;
        }

        .section {
            margin-bottom: 60px;
            padding: 30px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 20px;
            color: #2c3e50;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
        }

        .section h3 {
            color: #34495e;
            margin: 20px 0 10px 0;
            font-size: 1.3em;
        }

        .section p {
            margin-bottom: 15px;
            font-size: 1.1em;
            text-align: justify;
        }

        /* Education */
        .education-item {
            background: #f8f9fa;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
            border-left: 4px solid #3498db;
        }

        .education-item h4 {
            color: #2c3e50;
            margin-bottom: 5px;
        }

        .education-item .degree {
            font-weight: bold;
            color: #34495e;
            margin-bottom: 5px;
        }

        .education-item .institution {
            font-style: italic;
            color: #666;
            margin-bottom: 10px;
        }

        /* Research Areas */
        .research-areas {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .research-card {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #3498db;
            transition: transform 0.3s ease;
        }

        .research-card:hover {
            transform: translateY(-5px);
        }

        .research-card h4 {
            color: #2c3e50;
            margin-bottom: 10px;
        }

        /* Publications */
        .publication {
            background: #f8f9fa;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
            border-left: 4px solid #28a745;
        }

        .publication h4 {
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .publication .journal {
            font-style: italic;
            color: #666;
            margin-bottom: 10px;
        }

        .publication .status {
            font-weight: bold;
            color: #dc3545;
            margin-bottom: 10px;
        }

        .publication .links {
            margin-top: 10px;
        }

        .publication .links a {
            display: inline-block;
            margin-right: 10px;
            padding: 5px 10px;
            background: #3498db;
            color: white;
            text-decoration: none;
            border-radius: 3px;
            font-size: 0.9em;
            transition: background 0.3s ease;
        }

        .publication .links a:hover {
            background: #2980b9;
        }

        /* News Section */
        .news-item {
            padding: 15px;
            margin-bottom: 15px;
            background: #fff3cd;
            border-left: 4px solid #ffc107;
            border-radius: 5px;
        }

        .news-date {
            font-weight: bold;
            color: #856404;
            margin-bottom: 5px;
        }

        /* Awards */
        .award-item {
            background: #d1ecf1;
            padding: 15px;
            margin-bottom: 15px;
            border-left: 4px solid #17a2b8;
            border-radius: 5px;
        }

        .award-year {
            font-weight: bold;
            color: #0c5460;
            margin-bottom: 5px;
        }

        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 30px 0;
            margin-top: 60px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content h1 {
                font-size: 2em;
            }
            
            .nav-links {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }
            
            .contact-info {
                flex-direction: column;
                gap: 15px;
            }
            
            .section {
                padding: 20px;
            }
        }

        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }

        /* Hide sections by default for SPA effect */
        .section {
            display: none;
        }

        .section.active {
            display: block;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <h1>Jason Katz</h1>
                <p>PhD Candidate in Planning Studies</p>
                <p>University College London (UCL) | Bartlett School of Planning</p>
                <div class="contact-info">
                    <a href="mailto:jason.katz.21@ucl.ac.uk">📧 Email</a>
                    <a href="#cv">📄 CV</a>
                    <a href="https://scholar.google.com" target="_blank">🎓 Google Scholar</a>
                    <a href="https://orcid.org" target="_blank">🔗 ORCID</a>
                </div>
            </div>
        </div>
    </header>

    <nav>
        <div class="container">
            <ul class="nav-links">
                <li><a href="#about" class="nav-link active">About</a></li>
                <li><a href="#education" class="nav-link">Education</a></li>
                <li><a href="#research" class="nav-link">Research</a></li>
                <li><a href="#publications" class="nav-link">Publications</a></li>
                <li><a href="#teaching" class="nav-link">Teaching</a></li>
                <li><a href="#grants" class="nav-link">Grants & Awards</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
        </div>
    </nav>

    <main>
        <div class="container">
            <!-- About Section -->
            <section id="about" class="section active">
                <h2>About</h2>
                <p>I am a PhD candidate in Planning Studies at the Bartlett School of Planning, University College London (UCL). My research focuses on post-Olympic planning and urban development, examining London's extending 'Legacy' plans from 2012-2040 under the supervision of Susan Moore, Camillo Boano, and David Roberts.</p>
                
                <p>My work sits at the intersection of urban planning, property development, and community activism, with a particular focus on understanding how major urban interventions like the Olympics continue to shape cities long after the initial event. I am particularly interested in examining planning processes "from below" and exploring alternative approaches to urban development.</p>

                <p>I am actively involved with the Just Space Community Planning Network and have extensive research experience examining urban development in London, particularly around King's Cross and Olympic legacy sites. My interdisciplinary background spans urban studies, international business, and planning, with research experience across multiple continents.</p>

                <h3>Current Research</h3>
                <p><strong>PhD Dissertation:</strong> "Under the 'New Norm' of post-Olympic Planning: An examination of London's extending 'Legacy' plans, 2012-2040"</p>
                <p>This research investigates how Olympic planning paradigms have become normalized in London's planning practice, examining the ongoing influence of Olympic development models on urban planning and community displacement.</p>
            </section>

            <!-- Education Section -->
            <section id="education" class="section">
                <h2>Education</h2>
                
                <div class="education-item">
                    <h4>2023 - Present</h4>
                    <div class="degree">PhD Planning Studies</div>
                    <div class="institution">Bartlett School of Planning, University College London (UCL)</div>
                    <p><strong>Dissertation:</strong> "Under the 'New Norm' of post-Olympic Planning: An examination of London's extending 'Legacy' plans, 2012-2040"</p>
                    <p><strong>Supervisors:</strong> Susan Moore, Camillo Boano, David Roberts</p>
                </div>

                <div class="education-item">
                    <h4>2023</h4>
                    <div class="degree">MSc Urban Studies (Distinction)</div>
                    <div class="institution">Department of Geography, University College London (UCL)</div>
                    <p><strong>Thesis:</strong> "An Archaeology of Property Paradigms in the King's Cross Railway Lands"</p>
                </div>

                <div class="education-item">
                    <h4>2021</h4>
                    <div class="degree">MSc International Business (Summa Cum Laude)</div>
                    <div class="institution">George Washington University</div>
                    <p><strong>Thesis:</strong> "Residential Financialisation in the Narrativized City"</p>
                </div>

                <div class="education-item">
                    <h4>2020</h4>
                    <div class="degree">B.A. Urban Studies (Cum Laude), Minor in Spanish</div>
                    <div class="institution">George Washington University</div>
                    <p><strong>Special Interdisciplinary Major (SIM) Program & Global Bachelor's Program</strong></p>
                    <p><strong>Thesis 1:</strong> "Community Timescapes in the Narrativized City"</p>
                    <p><strong>Thesis 2:</strong> "Building 'Missing Middle Housing' in Northern Virginia: Possibilities in the Baugruppen Model and the Limits of International Housing Policy Transfer"</p>
                </div>

                <h3>International Exchanges</h3>
                <div class="education-item">
                    <h4>2017-2019</h4>
                    <div class="degree">International Exchange Programs</div>
                    <div class="institution">Multiple Universities</div>
                    <ul style="margin-left: 20px; margin-top: 10px;">
                        <li><strong>2019:</strong> Universidad Torcuato di Tella, Buenos Aires, Argentina</li>
                        <li><strong>2018:</strong> Pontificia Universidad Católica de Chile, Santiago, Chile</li>
                        <li><strong>2018:</strong> Fudan University, Shanghai, China</li>
                        <li><strong>2017:</strong> GWU Berlin Summer Exchange, Berlin, Germany</li>
                    </ul>
                </div>
            </section>

            <!-- Research Section -->
            <section id="research" class="section">
                <h2>Research Areas</h2>
                <div class="research-areas">
                    <div class="research-card">
                        <h4>Post-Olympic Planning</h4>
                        <p>Examining how Olympic development models influence long-term urban planning and community development.</p>
                    </div>
                    <div class="research-card">
                        <h4>Urban Development</h4>
                        <p>Investigating property paradigms and financialization in major urban redevelopment projects.</p>
                    </div>
                    <div class="research-card">
                        <h4>Community Planning</h4>
                        <p>Exploring planning "from below" and community-led approaches to urban development.</p>
                    </div>
                    <div class="research-card">
                        <h4>Housing Policy</h4>
                        <p>Analyzing alternative housing models and international policy transfer in urban contexts.</p>
                    </div>
                    <div class="research-card">
                        <h4>Critical Urban Studies</h4>
                        <p>Applying critical theoretical frameworks to understand contemporary urban transformations.</p>
                    </div>
                    <div class="research-card">
                        <h4>Opportunity Areas</h4>
                        <p>Examining London's strategic development areas and their impact on communities.</p>
                    </div>
                </div>

                <h3>Current Projects</h3>
                <div class="publication">
                    <h4>King's Cross from Below</h4>
                    <p>Collaborative research project examining community perspectives on the King's Cross redevelopment, co-led with Professor Michael Edwards.</p>
                </div>

                <div class="publication">
                    <h4>Wild Archaeologies</h4>
                    <p>Interdisciplinary workshop series exploring contemporary archaeological methodologies, co-convened with Nastassja Simensky.</p>
                </div>
            </section>

            <!-- Publications Section -->
            <section id="publications" class="section">
                <h2>Publications & Projects</h2>
                
                <h3>Books</h3>
                <div class="publication">
                    <h4>King's Cross from Below</h4>
                    <div class="journal">UCL Press</div>
                    <div class="status">Forthcoming</div>
                    <p><strong>Co-Editor with M Edwards.</strong> A comprehensive examination of community perspectives on the King's Cross redevelopment.</p>
                </div>

                <h3>Book Chapters</h3>
                <div class="publication">
                    <h4>"Hacking the Corporate Ownership of King's Cross"</h4>
                    <div class="journal">In M Edwards and J Katz (eds.), King's Cross Otherwise. UCL Press</div>
                    <div class="status">Forthcoming</div>
                    <p>Analysis of corporate ownership structures in major urban redevelopment projects.</p>
                </div>

                <div class="publication">
                    <h4>Introduction & Contributors' Dialogue</h4>
                    <div class="journal">In M Edwards and J Katz (eds.), King's Cross Otherwise. UCL Press</div>
                    <div class="status">Forthcoming</div>
                    <p><strong>Co-authored with M Edwards.</strong> Multiple chapters examining alternative approaches to understanding urban development.</p>
                </div>

                <div class="publication">
                    <h4>"A New Urban Park"</h4>
                    <div class="journal">In Bernstock, P., et. al. (2022). 'State of the Legacy Report'. UCL Urban Laboratory</div>
                    <div class="status">Published 2022</div>
                    <p>Analysis of post-Olympic urban park development and community access.</p>
                </div>

                <h3>Policy Publications</h3>
                <div class="publication">
                    <h4>Opportunity Areas & Mayoral Development Corporations</h4>
                    <div class="journal">Just Space - Submitted as evidence to the London Assembly</div>
                    <div class="status">2023</div>
                    <p><strong>Co-authored with M Edwards.</strong> Policy analysis examining London's strategic development mechanisms and their community impacts.</p>
                </div>

                <div class="publication">
                    <h4>Just Space memorandum on Opportunity Areas</h4>
                    <div class="journal">Just Space - Submitted as evidence to the London Assembly</div>
                    <div class="status">2022</div>
                    <p><strong>Co-authored with M Edwards and D Malaj.</strong> Community planning network response to London's development strategy.</p>
                </div>

                <h3>Conference Presentations</h3>
                <div class="publication">
                    <h4>"Occupy Surplus-value-of-life: A destituent planning grammar for rethinking value in precarious territories"</h4>
                    <div class="journal">The epistemic tangles of urban inhabitation workshop, University of Sheffield & Politecnico di Torino</div>
                    <div class="status">May 2024</div>
                    <p><strong>Co-presented with C Boano.</strong> Theoretical framework for alternative planning approaches in precarious urban contexts.</p>
                </div>

                <div class="publication">
                    <h4>"Taking Stock of Opportunity Areas"</h4>
                    <div class="journal">UCL-Just Space Knowledge Exchange Programme, Bartlett School of Planning</div>
                    <div class="status">July 2023</div>
                    <p><strong>Co-presented with M Edwards.</strong> Analysis of London's strategic development areas and community impacts.</p>
                </div>
            </section>

            <!-- Teaching Section -->
            <section id="teaching" class="section">
                <h2>Teaching Experience</h2>
                
                <h3>University College London (UCL)</h3>
                <div class="publication">
                    <h4>Cities, Space and Power</h4>
                    <div class="journal">Department of Geography - Autumn 2024</div>
                    <p><strong>Postgraduate Tutor.</strong> Core module for the MSc Urban Studies programme examining the relationship between urban space and power dynamics.</p>
                </div>

                <div class="publication">
                    <h4>Cities and Social Change</h4>
                    <div class="journal">Bartlett School of Planning - 2024</div>
                    <p><strong>Postgraduate Tutor.</strong> Second year undergraduate module exploring how cities respond to and drive social transformation.</p>
                </div>

                <h3>Teaching Philosophy</h3>
                <p>My teaching approach emphasizes critical engagement with urban planning theory and practice, encouraging students to examine planning processes from multiple perspectives, particularly those of affected communities. I believe in connecting theoretical frameworks to real-world case studies and encouraging students to develop their own critical analysis skills through collaborative learning and community engagement.</p>
            </section>

            <!-- Grants & Awards Section -->
            <section id="grants" class="section">
                <h2>Grants & Awards</h2>
                
                <div class="award-item">
                    <div class="award-year">2024-25</div>
                    <h4>Harriet's Trust Research Grant</h4>
                    <p><strong>Co-PI with Prof. Michael Edwards.</strong> 'King's Cross from Below' - Support for community-engaged research and publication.</p>
                </div>

                <div class="award-item">
                    <div class="award-year">2024</div>
                    <h4>UCL Institute for Advanced Study, Octagon Grant</h4>
                    <p><strong>Co-PI with Nastassja Simensky.</strong> 'Wild Archaeologies: Assembling the contemporary' - Interdisciplinary workshop series funding.</p>
                </div>

                <div class="award-item">
                    <div class="award-year">2019</div>
                    <h4>George Washington University, Columbian College Research Award</h4>
                    <p>Summer Research Project in Buenos Aires, Argentina: 'Community preservation and urbanisation of Villa 31'</p>
                </div>

                <h3>Research & Professional Experience</h3>
                <div class="publication">
                    <h4>Graduate Researcher</h4>
                    <div class="journal">Just Space Community Planning Network (2021 - Present)</div>
                    <p>Community-engaged research on London planning policy and development impacts.</p>
                </div>

                <div class="publication">
                    <h4>Research Assistant</h4>
                    <div class="journal">UCL Urban Laboratory (2022)</div>
                    <p>Research support for Olympic legacy and urban development studies.</p>
                </div>

                <h3>Academic Service</h3>
                <div class="publication">
                    <h4>PhD Representative</h4>
                    <div class="journal">Bartlett School of Planning, UCL (2024 - Present)</div>
                    <p>Student representation and advocacy within the planning department.</p>
                </div>
            </section>

            <!-- Contact Section -->
            <section id="contact" class="section">
                <h2>Contact</h2>
                <p><strong>Email:</strong> jason.katz.21@ucl.ac.uk</p>
                <p><strong>Office:</strong> Bartlett School of Planning, University College London</p>
                <p><strong>Mailing Address:</strong><br>
                   Bartlett School of Planning<br>
                   University College London<br>
                   Central House, 14 Upper Woburn Place<br>
                   London WC1H 0NN, United Kingdom</p>
                
                <h3>Affiliations</h3>
                <p><strong>Just Space Community Planning Network</strong> - Graduate Researcher</p>
                <p><strong>UCL Urban Laboratory</strong> - Research Associate</p>
                <p><strong>Bartlett School of Planning</strong> - PhD Representative</p>

                <h3>Recent News</h3>
                <div class="news-item">
                    <div class="news-date">November 2024</div>
                    <p>Co-convened "Wild Archaeologies II: Assembling the Contemporary" workshop with keynote lectures from Prof. Knut Ebeling, Prof. Ido Govrin, and Prof. JR Carpenter.</p>
                </div>

                <div class="news-item">
                    <div class="news-date">October 2024</div>
                    <p>Co-convened "King's Cross from Below" workshop, funded by the Great Northern Hotel, King's Cross.</p>
                </div>

                <div class="news-item">
                    <div class="news-date">June 2024</div>
                    <p>Participated in INURA Annual Conference in Malaga, Spain: "[Un]Attractive City: Breaking the Spell of Space Exploitation"</p>
                </div>
            </section>
        </div>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 Jason Katz. All rights reserved.</p>
            <p>University College London | Bartlett School of Planning</p>
        </div>
    </footer>

    <script>
        // Simple navigation system
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const sections = document.querySelectorAll('.section');

            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    // Remove active class from all nav links and sections
                    navLinks.forEach(nl => nl.classList.remove('active'));
                    sections.forEach(section => section.classList.remove('active'));
                    
                    // Add active class to clicked link
                    this.classList.add('active');
                    
                    // Show corresponding section
                    const targetId = this.getAttribute('href').substring(1);
                    const targetSection = document.getElementById(targetId);
                    if (targetSection) {
                        targetSection.classList.add('active');
                    }
                });
            });
        });
    </script>
</body>
</html>
