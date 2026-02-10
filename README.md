# 🌀 Learning Probability Density Function using GAN

**Objective:** Learning complex, non-parametric probability distributions from environmental data through adversarial optimization.

---

## 🛠️ 1. Methodology
The pipeline maps environmental features through a personalized non-linear transformation before feeding them into a minimax optimization framework.



**Pipeline:** `Data Collection` → `Pre-processing` → `Data Transformation` → `GAN Training` → `PDF Estimation` → `Result Analysis`

---

## 📄 2. Description
* **Dataset:** India Air Quality Dataset ($NO_2$ concentration).
* **Input Feature:** $NO_2$ values ($x$).
* **Transformation Logic:** $z = x + a_r \sin(b_r x)$.
* **Parameters ($r$ = Roll No):** * $a_r = 0.5 \times (r \pmod 7)$
  * $b_r = 0.3 \times ((r \pmod 5) + 1)$
* **Model Engine:** Generative Adversarial Network (GAN) with Gaussian noise $\mathcal{N}(0,1)$.
* **PDF Estimation:** Kernel Density Estimation (KDE).

---

## 📉 3. Input / Output
| Input | Output |
| :--- | :--- |
| $NO_2$ concentration ($x$) | Generated samples ($z_f$) |
| Gaussian noise | Estimated probability density |

---

## 🏆 4. Results
* **Implicit Learning:** GAN learns the distribution strictly from samples without analytical forms.
* **Mode Coverage:** Successfully captures multiple modes in the transformed space.
* **Stability:** Training remains stable post-convergence after 3000 epochs.
* **Fidelity:** Generated PDF shows high alignment with real data distribution.

---

## 📊 5. Visualization
* **KDE Mapping:** PDF plotted using KDE on GAN-generated samples.
* **Output:** Smooth, realistic density curves representing the learned manifold.



---

## 💻 6. Technologies Used
* **Languages:** Python
* **Data Ops:** NumPy, Pandas
* **Deep Learning:** PyTorch
* **Visualization:** Matplotlib, SciPy

---

## 🏁 7. Conclusion
The GAN successfully learns an unknown, non-parametric probability density function from transformed $NO_2$ data without assuming any prior analytical form.
