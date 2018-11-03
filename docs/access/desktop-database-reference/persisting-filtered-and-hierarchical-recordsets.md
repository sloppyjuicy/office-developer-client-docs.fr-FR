---
title: Conservation des jeux d’enregistrements hiérarchiques et filtrés
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13255bcd5cd40745a767b8aff9f49449b0127294
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946117"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Conservation des jeux d’enregistrements hiérarchiques et filtrés


**S’applique à**: Access 2013, Office 2013

Si la propriété [Filter](filter-property-ado.md) est activée pour le **jeu d'enregistrements**, seules les lignes accessibles via le filtre sont sauvegardées. Si le **jeu d'enregistrements** est hiérarchique, le **jeu d'enregistrements** enfant et ses enfants sont sauvegardés, y compris le **jeu d'enregistrements** parent. Si la méthode **Save** d'un **jeu d'enregistrements** enfant est invoquée, l'enfant et tous ces enfants sont enregistrés, mais pas le parent. Pour en savoir plus sur les **jeux d'enregistrements** hiérarchiques, reportez-vous au [Chapitre 9 : Mise en forme des données](chapter-9-data-shaping.md).


> [!NOTE]
> [!REMARQUE] Certaines restrictions s'appliquent lors de la sauvegarde de **jeux d'enregistrements** hiérarchiques (formes de données) au format XML. Pour en savoir plus, reportez-vous à la rubrique [Jeux d'enregistrements hiérarchiques dans XML](hierarchical-recordsets-in-xml.md).


