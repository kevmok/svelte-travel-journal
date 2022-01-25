<script>
    export let id;
    export let title;
    export let location;
    export let googleMapsUrl;
    export let startDate;
    export let endDate;
    export let description;
    export let imageUrl;

    let locationIcon = './images/location-icon.svg';
</script>

<section>
    <main>
        <img src={imageUrl} alt="" class="main-img" />
        <div class="info">
            <div class="location">
                <img src={locationIcon} alt="" class="location-icon" />
                <span class="location-country">
                    {location}
                </span>
                <a href={googleMapsUrl} class="location-url"
                    >View on Google Maps
                </a>
            </div>
            <h2>{title}</h2>
            <p class="date">{startDate} - {endDate}</p>
            <p class="description">{description}</p>
        </div>
    </main>
    <hr />
</section>

<style>
    section {
        margin: 0 auto;
        width: 73%;
    }

    main {
        display: flex;
        align-items: center;
        gap: 1.7rem;
    }

    .info {
    }

    hr {
        border: 1px solid #e5e5e5;
        margin: auto;
        width: 100%;
        margin: 2rem 0;
    }

    .main-img {
        object-fit: cover;
        height: 16.5rem;
        border-radius: 10px;
        width: 187.5px;
    }

    .location {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        gap: 0.3rem;
    }

    .location-icon {
        width: 0.7rem;
    }

    .location-country {
        color: #2b283a;
        letter-spacing: 0.2rem;
        text-transform: uppercase;
        padding-right: 0.7rem;
    }

    .location-url {
        color: #918e9b;
        text-decoration-line: underline;
    }

    h2 {
        color: #2b283a;
        font-weight: bold;
        font-size: 2.5rem;
        margin-top: 0.2rem;
        margin-bottom: 1.4rem;
    }

    .date {
        color: #2b283a;
        font-weight: bold;
        margin-bottom: 0;
        padding-bottom: 0.8rem;
    }

    .description {
        color: #2b283a;
        line-height: 150%;
        margin-bottom: 0;
        margin-top: 0;
    }
</style>
