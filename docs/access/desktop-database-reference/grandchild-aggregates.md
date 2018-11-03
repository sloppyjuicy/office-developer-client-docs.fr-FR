---
title: Agrégats de petits-enfants
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7576eb8e1555ab8b00d2800242c7be24baca58
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947937"
---
# <a name="grandchild-aggregates"></a>Agrégats de petits-enfants


**S’applique à**: Access 2013, Office 2013

Un *nom d’alias-chapitre* (généralement avec le mot clé AS) peut être donnée à la colonne de chapitre créée dans une clause d’une commande shape. Vous pouvez identifier une colonne quelconque dans n’importe quel chapitre de l' **objet Recordset** mis en forme avec un nom complet identifiant l’enfant contenant la colonne. Par exemple, si le chapitre parent, chap1, contient un chapitre enfant, chap2, qui a une colonne quantité, montant, puis le nom complet est Chap1.Chap2.mnt. Le nom qualifié peut ensuite être utilisé en tant qu’argument à une des fonctions d’agrégation (somme, moyenne, MAX, MIN, COUNT, STDEV ou toute).

