<style>
    h1 {
        margin: 0px;
        padding: 0px;
        font-size: 50px;
    }
    section {
        border-bottom: 1px solid var(--accent);
        padding: 30px;
    }
    
    .headshot {
        border-radius: 50%;
        border: 2px solid var(--accent);
        display: flex;
        float: right;
    }

    row {
        display: inline-flex;
        justify-content: space-between;
        flex-grow: 1;
    }

    @media only screen and (min-width: 701px) {
        row {
            flex-direction: row;
        }
        .headshot {
            width: 40%;
        }
    }
 
    @media only screen and (max-width: 700px) {
        row {
            flex-direction: column;
            
        }
        .headshot {
            width: 80%;
        }
    }
</style>

<section>
    <row>
        <div>
            <h1>Other</h1>
            <p>
                I also love the beach so much it is the best place and I am a beach lover because the beach is beach the end period.
            </p>
        </div>
        <img alt="Headshot" src="headshot.jpg" class="headshot" />
    </row>
</section>
