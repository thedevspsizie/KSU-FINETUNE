# KSU-FineTune

**Módulo de ajuste fino (fine tuning) para Android com KernelSU**, focado em **estabilidade**, **eficiência energética** e **equilíbrio do sistema**.

> ❗ **Este não é um módulo gamer, nem um módulo de benchmark.**

---

## 📱 Ambiente de Testes

Este módulo foi testado **apenas** no seguinte ambiente:

* **ROM:** HyperOS 3 (China Port)
* **Android:** 15
* **Kernel:** Stock (original da ROM, não modificado)
* **Root:** KernelSU

### ⚠️ Aviso importante

* HyperOS **Global** ❌ *não testado*
* HyperOS **2.x** ❌ *não testado*
* **Kernels modificados** ❌ *não suportados*

> O uso fora desse ambiente é **por conta e risco do usuário**.

---

## 🎯 Objetivo do Módulo

O **KSU-FineTune** foi criado para:

* Melhorar a **fluidez geral** do sistema
* Reduzir **wakelocks desnecessários**
* Otimizar **I/O** e **latência de disco**
* Ajustar parâmetros de **memória (VM)** de forma segura
* Reduzir **aquecimento** em uso diário e jogos

Tudo isso **mantendo estabilidade**, sem agressividade.

---

## 🧠 Filosofia do Projeto

* RAM cheia **não é problema**
* Menos tweaks = **mais estabilidade**
* Android moderno já gerencia bem os recursos
* O módulo apenas **corrige excessos**

> *O melhor ajuste é aquele que você não percebe, apenas sente o sistema mais estável.*

---

## ⚙️ O que o Módulo Faz

### 🔹 1. Energia e WakeLocks

* Não bloqueia wakelocks críticos do sistema
* Reduz ativações desnecessárias
* Permite **deep sleep real**
* Compatível com **kernels stock**

---

### 🔹 2. Otimização de I/O

* Ajuste de `read_ahead_kb`
* Ajuste de `nr_requests`
* Mantém o **scheduler padrão** do kernel
* Reduz micro travamentos e *stutter*

---

### 🔹 3. Ajustes de Memória (VM)

* Ajuste de escrita em disco
* Melhor equilíbrio entre **cache** e **flush**
* Menor pressão de I/O em segundo plano

---

## ❌ O que o Módulo NÃO Faz

* ❌ Overclock de CPU ou GPU
* ❌ Alteração de governors
* ❌ Modificação de kernel
* ❌ Economia extrema de bateria
* ❌ Kill agressivo de processos

> Este módulo prioriza **segurança** e **previsibilidade**.

---

## 🧪 Como Verificar se Está Funcionando

### WakeLocks

```sh
dumpsys power | grep -i wake
```

### Estado de energia

```sh
dumpsys power | grep -i mWakefulness
```

### I/O

```sh
cat /sys/block/mmcblk0/queue/read_ahead_kb
cat /sys/block/mmcblk0/queue/nr_requests
cat /sys/block/mmcblk0/queue/scheduler
```

### Memória

```sh
cat /proc/sys/vm/dirty_expire_centisecs
cat /proc/sys/vm/dirty_writeback_centisecs
```

---

## ⚠️ Recomendações de Uso

* Não use junto com **outros módulos agressivos**
* Não combine com **kernels modificados**
* Sempre tenha **backup** antes de testar

---

## 🧩 Compatibilidade

| Item               | Suporte        |
| ------------------ | -------------- |
| KernelSU           | ✅              |
| Magisk             | ❌              |
| Kernel Stock       | ✅              |
| Kernel Modificado  | ❌              |
| HyperOS China Port | ✅              |
| HyperOS Global     | ⚠️ Não testado |

---

## 🐞 Reportando Problemas

Ao abrir uma *issue*, informe:

* Modelo do dispositivo
* ROM (China / Global / Port)
* Versão do Android
* Kernel (stock ou modificado)
* Versão do KernelSU

> Issues sem essas informações **podem ser ignoradas**.

---

## 📜 Aviso Legal

Este módulo é fornecido **como está**, sem garantias. O autor não se responsabiliza por danos, perda de dados ou instabilidade.

---

## 🙏 Créditos

Criado por **Spizie**
Testes e ajustes feitos em uso real, com foco em **estabilidade** e **uso diário**.


O uso fora desse ambiente é por conta e risco do usuário.


---

🎯 Objetivo do Módulo

O KSU-FineTune foi criado para:

Melhorar a fluidez geral do sistema

Reduzir wakelocks desnecessários

Otimizar I/O e latência de disco

Ajustar parâmetros de memória (VM) de forma segura

Reduzir aquecimento em uso diário e jogos


Tudo isso mantendo estabilidade, sem agressividade.


---

🧠 Filosofia do Projeto

RAM cheia não é problema

Menos tweaks = mais estabilidade

Android moderno já gerencia bem recursos

O módulo apenas corrige excessos


> O melhor ajuste é aquele que você não percebe, apenas sente o sistema mais estável.




---

⚙️ O que o Módulo Faz

🔹 1. Energia e WakeLocks

Não bloqueia wakelocks críticos do sistema

Reduz ativações desnecessárias

Permite deep sleep real

Compatível com kernels stock



---

🔹 2. Otimização de I/O

Ajuste de read_ahead_kb

Ajuste de nr_requests

Mantém scheduler padrão do kernel

Reduz micro travamentos e stutter



---

🔹 3. Ajustes de Memória (VM)

Ajuste de escrita em disco

Melhor equilíbrio entre cache e flush

Menor pressão de I/O em segundo plano



---

❌ O que o Módulo NÃO Faz

❌ Overclock de CPU ou GPU

❌ Alteração de governors

❌ Modificação de kernel

❌ Economia extrema de bateria

❌ Kill agressivo de processos


Este módulo prioriza segurança e previsibilidade.


---

🧪 Como Verificar se Está Funcionando

WakeLocks:

dumpsys power | grep -i wake

Estado de energia:

dumpsys power | grep -i mWakefulness

I/O:

cat /sys/block/mmcblk0/queue/read_ahead_kb
cat /sys/block/mmcblk0/queue/nr_requests
cat /sys/block/mmcblk0/queue/scheduler

Memória:

cat /proc/sys/vm/dirty_expire_centisecs
cat /proc/sys/vm/dirty_writeback_centisecs


---

⚠️ Recomendações de Uso

Não use junto com outros módulos agressivos

Não combine com kernels modificados

Sempre tenha backup antes de testar



---

🧩 Compatibilidade

Item	Suporte

KernelSU	✅
Magisk	❌
Kernel Stock	✅
Kernel Modificado	❌
HyperOS China Port	✅
HyperOS Global	⚠️ Não testado



---

🐞 Reportando Problemas

Ao abrir uma issue, informe:

Modelo do dispositivo

ROM (China / Global / Port)

Versão do Android

Kernel (stock ou modificado)

Versão do KernelSU


Issues sem essas informações podem ser ignoradas.


---

📜 Aviso Legal

Este módulo é fornecido como está, sem garantias. O autor não se responsabiliza por danos, perda de dados ou instabilidade.


---

🙏 Créditos

Criado por Spizie
Testes e ajustes feitos em uso real, foco em estabilidade e uso diário.
