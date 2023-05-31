#### Project: Juypter-Tensorflow-Service

#### Pass-ID: X9448776

#### Author: Atakan Çetinkaya

#### Created: 30.05.2023

#### Description: This .md (README.md) File is installing all necessary configs for the JP-Notebook combined with Tensorflow

#### File Name: README.md

#### Version: v1.0

---

<!-- PROJECT SHIELDS -->

<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/atakancetinkaya/github-how-to/blob/main/logo_by_a-cetinkaya.png">
    <img src="https://github.com/atakancetinkaya/github-how-to/blob/main/logo_by_a-cetinkaya.png" alt="Logo" width="250" height="250">
  </a>

  <h3 align="center">My Juypter-Tensorflow-Service Guide</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">My Juypter-Tensorflow-Service Content</a>
      <ul>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

---

## My Juypter-Tensorflow-Service Content

This .md (README.md) explains, what this Juypter-Tensorflow-Service exactly does.

Use the `README.md` to get started.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

This is the Guide to for the Juypter-Tensorflow-Service which is created to show the installation and the handling of the "JTS" Service

---

1.0) First of all, apply the following manifest file with the following command:

```sh
kubectl apply -f jupyter-tensorflow.yaml
```

---

1.1) Execute the following command to check the state of the resources:

kubectl get deploy,pod,pvc,pv,svc -n demo

---

1.2) Get the Logs from the "tensorflow-jupyter" pod with the following command:

```sh
kubectl logs pod/tensorflow-jupyter-7c8685d949-j6jtt -n demo
```

---

1.3) To even access the Pod (tensorflow-jupyter-<pod-id>) you have to execute the command below:

```sh
kubectl port-forward pod/tensorflow-jupyter-7c8685d949-j6jtt 8888:8888 -n demo
```

1.3.1) If you prefer a more straightforward approach, you can use the "pkill" command to terminate the "kubectl port-forward" process directly:

```sh
pkill -f "kubectl port-forward"
```

1.3.2) But if you have multiple instances of kubectl port-forward running, you can use the killall command to terminate all instances at once

```sh
killall "kubectl port-forward"
```

---

1.4) After executing step "1.2)" copy and paste the following URL with the token into the URL bar:

```sh
http://127.0.0.1:8888/?token=642e3cdf1958915316bf36119f389badd235f9aff26ee7ce
```

---

1.5) If you work on your local Client step "1.4)" should be enough, if you work on a Cloud-Server like GCP or AWS, you have to execute the following command below too:

```sh
ssh -L 8888:localhost:8888 <external-ip-of-masternode>
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

<!-- USAGE EXAMPLES -->

## Usage

- This is a short Demo how to use those single commands

<img src="https://github.com/atakancetinkaya/k8s-jupyter-tensorflow/blob/main/screenshots_for_usage/step_1.png" alt="SS-1">

<img src="https://github.com/atakancetinkaya/k8s-jupyter-tensorflow/blob/main/screenshots_for_usage/step_2.png" alt="SS-2">

<img src="https://github.com/atakancetinkaya/k8s-jupyter-tensorflow/blob/main/screenshots_for_usage/step_3.png" alt="SS-3">

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

Your Name - [LinkedIn](https://www.linkedin.com/in/atakan-%C3%A7etinkaya-28a34b226/) - atakan.cetinkaya01@gmail.com

Project Link: [GitHub-Juypter-Tensorflow-Service](https://github.com/atakancetinkaya/k8s-jupyter-tensorflow)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

On this space you will find a list of resources which can be helpful.

- [README.md](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
`````
