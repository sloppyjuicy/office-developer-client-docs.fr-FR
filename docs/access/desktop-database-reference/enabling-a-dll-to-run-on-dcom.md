---
title: Configuration d'une DLL pour son exécution sur DCOM
TOCTitle: Enabling a DLL to Run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eeec1109d2e352d43eaaa66a7e081123d7f388ee
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937714"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="2902d-102">Configuration d'une DLL pour son exécution sur DCOM</span><span class="sxs-lookup"><span data-stu-id="2902d-102">Enabling a DLL to Run on DCOM</span></span>


<span data-ttu-id="2902d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2902d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2902d-104">Les étapes suivantes décrivent comment activer une bibliothèques de liens dynamiques objet métier utiliser DCOM et Microsoft Internet Information Services (protocole HTTP) via les Services de composants.</span><span class="sxs-lookup"><span data-stu-id="2902d-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="2902d-p101">Créez un package vide dans le composant logiciel enfichable MMC Services de composants. Vous devez utiliser le composant logiciel enfichable MMC Services de composants pour créer un package et pour y ajouter la DLL. Cette opération rend le fichier.dll accessible via DCOM mais supprime en revanche l'accessibilité via IIS. (Si vous recherchez la DLL dans le Registre, vous constaterez que la clé **Inproc** est vide. La définition de l'attribut Activation ajoute une valeur à la clé **Inproc**. Ce dernier point est expliqué plus loin dans cette rubrique.)</span><span class="sxs-lookup"><span data-stu-id="2902d-p101">Create a new empty package in the Component Services MMC snap-in. You will use the Component Services MMC snap-in to create a package and add the DLL into this package. This makes the .dll accessible through DCOM, but it removes the accessibility through IIS. (If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="2902d-p102">Installez un objet métier dans le package. - ou - Importez l'objet [RDSServer.DataFactoryDataFactory, objet (RDSServer)](datafactory-object-rdsserver.md) dans le package.</span><span class="sxs-lookup"><span data-stu-id="2902d-p102">Install a business object into the package. -or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="2902d-p103">Affectez à l'attribut Activation du package la valeur : **Dans le processus du créateur** (application bibliothèque). Pour pouvoir accéder à la DLL via DCOM et IIS sur le même ordinateur, vous devez attribuer à l'attribut Activation du composant dans le composant logiciel enfichable MMC Services de composants la valeur : **Dans le processus du créateur**. Vous remarquerez qu'une clé serveur **Inproc** a été ajoutée dans le Registre, pointant vers une DLL de substitution des services de composants.</span><span class="sxs-lookup"><span data-stu-id="2902d-p103">Set the Activation attribute for the package to **In the creator's process** (Library application). To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in. After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>

