---
title: Configuration d’une DLL pour son exécution sur DCOM
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9feb189221a1d447e6c2e0242240ca13784b7fe
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946460"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>Configuration d’une DLL pour son exécution sur DCOM


**S’applique à**: Access 2013, Office 2013

Les étapes suivantes décrivent comment activer une bibliothèques de liens dynamiques objet métier utiliser DCOM et Microsoft Internet Information Services (protocole HTTP) via les Services de composants.

1.  Créez un package vide dans le composant logiciel enfichable MMC Services de composants. Vous devez utiliser le composant logiciel enfichable MMC Services de composants pour créer un package et pour y ajouter la DLL. Cette opération rend le fichier.dll accessible via DCOM mais supprime en revanche l'accessibilité via IIS. (Si vous recherchez la DLL dans le Registre, vous constaterez que la clé **Inproc** est vide. La définition de l'attribut Activation ajoute une valeur à la clé **Inproc**. Ce dernier point est expliqué plus loin dans cette rubrique.)

2.  Installez un objet métier dans le package. - ou - Importez l'objet [RDSServer.DataFactoryDataFactory, objet (RDSServer)](datafactory-object-rdsserver.md) dans le package.

3.  Affectez à l'attribut Activation du package la valeur : **Dans le processus du créateur** (application bibliothèque). Pour pouvoir accéder à la DLL via DCOM et IIS sur le même ordinateur, vous devez attribuer à l'attribut Activation du composant dans le composant logiciel enfichable MMC Services de composants la valeur : **Dans le processus du créateur**. Vous remarquerez qu'une clé serveur **Inproc** a été ajoutée dans le Registre, pointant vers une DLL de substitution des services de composants.

