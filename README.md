# Project-1
                          ---Data.jsx---
import { VscLaw } from "react-icons/vsc";
import { RiBankLine } from "react-icons/ri";
import { AiOutlineLaptop} from "react-icons/ai";
import { MdOutlineRealEstateAgent, MdOutlineAddHomeWork } from "react-icons/md";
import { AiOutlineInsurance } from "react-icons/ai";



export const Data = [
    {
     icon:<VscLaw />,
     title: 'Corporate Law',
     description:'Focusing on advisting and representing corporations, their executives, and shareholders on various legal matters. This includes mergers and acquisitions, intellectual property rights, corporate governance, and securities law.'
    },
    
    {
        icon:<RiBankLine />,
        title: 'Banking&Finance',
        description:'We are specialized in legal issues concerning the transaction and regulation of financial instruments and institucions. This involve issues like lending agreements, regulatory compliance, securitization, and capital markets.'
    },
    
    {
        icon:<AiOutlineLaptop />,
        title: 'ICT Sector',
        description:'We help clients navigate through regulatory compliance, data protection, intellectual property issues, and e-commerce law. We alse work on contracts involving software licenses, cloud computing agreements, and technology transfers.'
    },
    
    {
        icon:<MdOutlineRealEstateAgent />,
        title: 'Real Estate',
        description:'We guide our clients through property transactions, ensuring that all regulations are met and that contracts are legally sound. This can include zoning issues, title searches, and financing'
    },
    
    {
        icon:<AiOutlineInsurance  />,
        title: 'Insurance',
        description:'We help clients with legal issues concerning insurance policies and claims like policy interpretation, insurance fraud investigations, and litigation over denied claims.'
    },
    
    {
        icon:<MdOutlineAddHomeWork />,
        title: 'Laborator&Employment',
        description:'We can help on matters involving employer-employee relationships. Including employment contracts, workplace discrimination, employee benefits, and collective bargaining agreements.'
    }
    

]


export const FooterData = [
    {
        category: 'ABOUT',
        links:[
            {
                link:'Our Story',
                to:'/'
            },
            
            {
                link:'Our Team',
                to:'/'
            },
            {
                link:'Careers',
                to:'/'
            },
            {
                link:'Client&Partners',
                to:'/'
            }
        ]
    },

    {
        category: 'SERVICES',
        links:[
            {
                link:'Practice Area',
                to:'/'
            },
            {
                link:'Solutions',
                to:'/'
            },
            {
                link:'Legal Tech',
                to:'/'
            },
            {
                link:'Case Studies',
                to:'/'
            }
        ]
    },

    {
        category: 'RESOURCES',
        links:[
            {
                link:'Contact Us',
                to:'/'
            },
            {
                link:'Latest News',
                to:'/'
            },
            {
                link:'Insights',
                to:'/'
            },
            {
                link:'Legal Notices',
                to:'/'
            }
        ]
    }
]                          


                                    ------Footer.jsx------------
import React from 'react'
import { Link } from 'react-router-dom'
import './Footer.scss'
import { FooterData } from './Data'


const Footer = () => {
  return (
    <div className='footer'>
       {FooterData.map((props) => {
          return(
            <div className='col'>
               <h6>{props.category}</h6>
               <div className='links'>
               {props.links.map((l) => {
                return(
                    <Link key={l.to} to={l.to}>{l.link}</Link>
                )
               })}
               </div>
            </div>
          )
       })}
    </div>
  )
}

export default Footer                        


               -------------------footer.scss-----------------
.footer{
    background: rgb(20, 20, 20);
    color: #fff;
    padding: 5%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;

    .col{
        width: fit-content;
        margin: 25px 50px;
    }
    a{
        color: #fff;
        font-size: 20px;
        margin: 10px;
    }
    .links{
        display: flex;
        flex-direction: column;
    }
    h6{
        font-size: 22px;
        margin-bottom: 15px;
    }
}               


                               -----------NavData.jsx-------------------
import { VscLaw } from "react-icons/vsc";
import { RiBankLine } from "react-icons/ri";
import { AiOutlineLaptop, AiOutlineInsurance} from "react-icons/ai";
import { MdOutlineRealEstateAgent, MdOutlineAddHomeWork } from "react-icons/md";
import { FaFileContract } from "react-icons/fa";
import { MdOutlineEnergySavingsLeaf } from "react-icons/md";
import { SlEnvolopeLetter } from "react-icons/sl";
import { BsJournalMinus } from "react-icons/bs";
import { MdFamilyRestroom } from "react-icons/md";
import { GiCrimeSceneTape } from "react-icons/gi";



export const NavData = [
    {
        icon:<VscLaw/>,
        title:'title1',
        to:'/'
    },
    {
        icon:<RiBankLine/>,
        title:'title2',
        to:'/'
    },
    {
        icon:<AiOutlineLaptop/>,
        title:'title3',
        to:'/'
    },
    {
        icon:<AiOutlineInsurance/>,
        title:'title4',
        to:'/'
    },
    {
        icon:<MdOutlineRealEstateAgent/>,
        title:'title5',
        to:'/'
    },
    {
        icon:<MdOutlineAddHomeWork/>,
        title:'title6',
        to:'/'
    },

    {
        icon:<FaFileContract/>,
        title:'title7',
        to:'/'
    },
    {
        icon:<MdOutlineEnergySavingsLeaf/>,
        title:'title8',
        to:'/'
    },
    {
        icon:<SlEnvolopeLetter/>,
        title:'title9',
        to:'/'
    },
    {
        icon:<BsJournalMinus/>,
        title:'title10',
        to:'/'
    },
    {
        icon:< MdFamilyRestroom />,
        title:'title11',
        to:'/'
    },
    {
        icon:<GiCrimeSceneTape />,
        title:'title12',
        to:'/'
    }
]    

                          -------Our Area.jsx-----------------
import React from 'react'
import './ourarea.scss'
import { Data } from './Data'

const OurArea = () => {
  return (
    <section className="practice-areas">
      <h1>Our Practice Area 
      <div className="view-all-button">
      <span>VIEW ALL AREAS</span>
      <div className="arrow">&#10142;</div>
      </div> 
      </h1>
    <div className='area'>
        {Data.map((props) => {
            return(
                <div className='item'>
                  <div className='icon'>{props.icon}</div>
                  <h6>{props.title}</h6>
                  <p>{props.description}</p>
                </div>
            )
        })}

    </div>
    </section>
  )
}

export default OurArea                          

                                  ----------------------ourarea.scss---------
h1{
    font-size: 70px;
    margin: 40px 70px;
    

.view-all-button {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    height: 100px;
    border: 2px solid #000;
    border-radius: 50%;
    text-align: center;
    font-size: 14px;
    color: #000;
    font-weight: bold;
    position: relative;
    transition: transform 0.3s ease;
    cursor: pointer;
    margin: 0 90%;
    
  }
}
  .view-all-button:hover {
    transform: scale(1.1);
  }
  
  .view-all-button .arrow {
    position: absolute;
    right: 10px;
    bottom: 10px;
    font-size: 20px;
  }
.area{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin: 5%;
    
    .item{
        width: 30%;
        margin: 40px 0;
       
    }
    .icon{
        font-size: 50px;
        color: rgb(241, 208, 16);
    }
    h6{
        
        font-size: 30px;
        margin-bottom: 20px;

    }
    p{
        
        font-size: 15px;
        font-family: Arial, Helvetica, sans-serif;
    }
}

                                      -----------------Nav.jsx------------------------------
import React from 'react'
import { Link } from 'react-router-dom'
import './Nav.scss'
import { GoLaw } from "react-icons/go";
import { MdKeyboardArrowDown } from 'react-icons/md';
import { FaPhoneAlt } from "react-icons/fa";
import ServiceMegaMenu from './ServiceMegaMenu';

const Nav = () => {
  return (
    <div className='nav'>
        <Link to='/' className='title'>< GoLaw/>LAWKOS</Link>
     
     <div className='links'>
    <div className='nav-link'>
        <Link to='/' className='inner-link'>About</Link>
      </div>
    <div className='nav-link'>
        <Link to='/' className='inner-link'> Services<MdKeyboardArrowDown/></Link>
        <ServiceMegaMenu />
    </div>
    <div className='nav-link'>
        <Link to='/' className='inner-link'>Resources<MdKeyboardArrowDown/></Link>
     </div>
     <div className='nav-link'>
        <Link to='/' className='inner-link'>News</Link>
      </div>
      <div className='nav-link'>
        <Link to='/' className='inner-link'>Careers</Link>
      </div>
    </div>

    <div className='auth'>
    <Link to='/' className='phone-nr'><FaPhoneAlt/>+38345500500</Link>
    <Link to='/' className='contact-us'>Contact Us</Link>
    </div>

    </div>
  )
}

export default Nav



                                      ----------------Nav.scss---------------
.nav{
    padding: 15px 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .title{
        color: black;
        display: flex;
        align-items: center;
        font-size: 22px;
        svg{
            font-size: 40px;
            margin-right: 6px;

        }
    }
    .links{
        display: flex;
    }
    .nav-link {
      margin: 0 px;
      padding: 5px 10px;
      position: relative;
      .inner-link svg{
        transition: 0.25s;
      }
      &:hover{
        .nav-megamenu{
            display: flex;
        }
        .inner-link svg{
            transform: rotate(-180deg);
        }
      }
    }
    .inner-link{
        font-size: 15px;
        color: black;
        display: flex;
        align-items: center;
    }
    .auth a{
        font-size: 16px;
        
        padding: 0 5px;
        padding: 10px 15px;
        svg{

            margin-right: 5px;
            font-size: 15px;
        }
    }

    .phone-nr{
        color: black;
    }
    .contact-us{
        color: white;
         border: 1px solid;
        border-radius: 30px;
        background: black;
        
    }
    .nav-megamenu{
        background: #fff;
        position: absolute;
        width: 1200px;
        height: 500px;
        left: -500px;
        border-radius: 10px;
        padding: 25px;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        display: none;
        .menu-link{
        width: 33%;
        padding: 10px 15px;
        &:hover{
            border: 1px solid;
        }
        }
        .menu-link a{
            display: flex;
            align-items: center;
        }
        .icon{
            width: 70px;
            font-size: 30px;
            color: gold;
        }
        h6{
            width: 50px;
            font-size: 20px;
            color: black;
        }
    }
}


                  -----------------------------ServiceMegaMenu-----------------
import React from 'react'
import { Link } from 'react-router-dom'
import { NavData } from './components/NavData'

const ServiceMegaMenu = () => {
  return (
    <div className='nav-megamenu'>
        {NavData.map((props) => {
            return(
                <div className='menu-link'>
                 <Link to={props.to}>
                 <div className='icon'>{props.icon}</div>
                 <div className='block'>
                  <h6>{props.title}</h6>
                 </div>
                 </Link>
                </div> 
            )
        })}

    </div>
  )
}

export default ServiceMegaMenu



