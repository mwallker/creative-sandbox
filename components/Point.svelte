<style>
  :root {
    --transition-duration: 200ms;
    --normal-color: #a1a1a1;
    --size: 11px;
    --border-: 5px;
    --pointOffset: -6px;
  }

  .point {
    font-size: 0.75rem;
    opacity: 0.7;
    position: absolute;
    color: var(--normal-color);
  }

  .point:hover {
    opacity: 1;
    cursor: pointer;
  }

  .point > i {
    border-radius: 50%;
    border: var(--pointBorder) solid var(--gridNormalColor);
    height: var(--pointSize);
    left: var(--pointOffset);
    position: absolute;
    top: var(--pointOffset);
    width: var(--pointSize);
    transform: none;
  }

  .point > span.coordinates {
    display: none;
  }

  .point:hover > span.coordinates {
    display: inline-block;
  }

  .point > span.label {
    padding: 0 0 0 5px;
  }

  .point.selected {
    font-weight: bold;
    opacity: 0.9;
  }

  .point.selected > i {
    background-color: var(--gridNormalColor);
  }

  .joint {
    font-size: 12px;
    color: var(--jointLightColor);
  }

  .joint > i {
    border-color: var(--jointDarkColor);
    background-color: var(--jointLightColor);
  }

  .target {
    font-size: 12px;
    color: var(--targetLightColor);
  }

  .target > i {
    border-color: var(--targetDarkColor);
    background-color: var(--targetLightColor);
  }

  @media screen and (max-width: 500px) {
    .point > span.label {
      padding: 0 0 0 10px;
    }

    .point > i {
      --pointSize: 19px;
      --pointBorder: 8px;
      --pointOffset: -10px;
    }
  }
</style>