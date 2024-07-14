# Kim-Ornis-React-Notes
React Notes

***** You will need https://nodejs.org *****

***** You will need to add the following in the terminal: npm create vite@latest *****
***** select a project name *****
***** Select a framework *****
***** select a variant Choose JavaScript *****
***** then run the comands that the terminal gives you *****

***** Src folder = this is where you spend most of your time coding *****
***** Assets folder = this is for pics, videos, etc *****
***** main.jsx = is your main javascript file *****
***** App.jsx = this is your route component all the other components will route to this component *****

***** Props = read only properties that are shared between components. A parent compnent can send data to a child component. <Component key=value /> *****

    *** App.jsx: ***

    import Students from './Students.jsx'

    function App(){
    return(
      <>
        <Students name="Kim" age={29} isStudents={true} />
        <Students name="Sam" age={20} isStudents={fale} />
        <Students name="Tim" age={45} isStudents={true} />
        <Students name="jim" age={99} isStudents={false} />
      </>
     );
    }

     *** Students.jsx Component: ***

          import PropTypes from 'prop-types'
          
          function Students(props){
               return(
                   <div>
                     <p>Name: {props.name}<p>
                     <p>Age: {props.age}<p>
                     <p>Students: {props.isStudents ? "Yes" : "No"}<p>
                   </div>
                 );  
                 }
                Students.propTypes = {
                  name: PropTypes.string,
                  name: PropTypes.number,
                  name: PropTypes.bool,
                  }
              export default Students



***** CLICK EVENT = An interaction when a user clicks on a component we can respond to clicks by passing a callback to the onclick event handle *****


    *** App.jsx: ***

    import Students from './Students.jsx'

    function App(){
    return(
      <>
        <Students name="Kim" age={29} isStudents={true} />
        <Students name="Sam" age={20} isStudents={fale} />
        <Students name="Tim" age={45} isStudents={true} />
        <Students name="jim" age={99} isStudents={false} />
      </>
     );
    }

     *** Button.jsx Component: ***
          
          function Button(){
             const handleClick = () => console.log("OUCH");
             const handleClick2 = (name) => console.log('${name} stop clicking me');
             
             return(<button onclick={() => handleClick2("Bro")}>Click me</button>);
            }
              export default Button




             
