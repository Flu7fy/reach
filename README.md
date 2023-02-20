# 
import './App.css';
import Header from './components/layout/Header';
import React, { useState } from 'react';


export default App;

//tehdään app funktio
function App() {
  const [jobs, setJobs] = useState(initJobs);

const rows = () => jobs.map(job =>{
    return <p key={job.id}>{job.tyotehtava}</p>
})

return ( 
      <div>w
        <div className="container">
          teksti tähän
        </div>
      </div>
      
)};

const initJobs = []
const [jobs, setJobs] = useState(initJobs);
fetch('http://gis.vantaa.fi/rest/tyopaikat/v1/kaikki')
.then(response => response.json())
.then(json=>setJobs([...json]));

<Header />





{rows()}
