---
title: Agrégats petit-enfant
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722157"
---
# <a name="grandchild-aggregates"></a>Agrégats petit-enfant


**S’applique à**: Access 2013, Office 2013

Un *nom d’alias-chapitre* (généralement avec le mot clé AS) peut être donnée à la colonne de chapitre créée dans une clause d’une commande shape. Vous pouvez identifier une colonne quelconque dans n’importe quel chapitre de l' **objet Recordset** mis en forme avec un nom complet identifiant l’enfant contenant la colonne. Par exemple, si le chapitre parent, chap1, contient un chapitre enfant, chap2, qui a une colonne quantité, montant, puis le nom complet est Chap1.Chap2.mnt. Le nom qualifié peut ensuite être utilisé en tant qu’argument à une des fonctions d’agrégation (somme, moyenne, MAX, MIN, COUNT, STDEV ou toute).

