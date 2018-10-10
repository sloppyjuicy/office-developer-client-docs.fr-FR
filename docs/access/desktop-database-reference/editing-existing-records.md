---
title: Modification d'enregistrements existants
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 274cd7667506159e2309fffb3596781c004f7006
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470963"
---
# <a name="editing-existing-records"></a>Modification d'enregistrements existants


**S’applique à**: Access 2013 | Office 2013

Pour modifier des enregistrements existants, allez dans la ligne que vous souhaitez modifier et changez la propriété **Value** des champs à modifier.Pour en savoir plus sur la propriété **Field** de l'objet **Field**, reportez-vous au [Chapitre 3 : Examen des données](chapter-3-examining-data.md). Selon le type de votre curseur, utilisez les méthodes **Update** ou **UpdateBatch** pour renvoyer les modifications à la source de données. Pour en savoir plus, reportez-vous au [Chapitre 5 : Mise à jour et conservation des données](chapter-5-updating-and-persisting-data.md).

L'utilisation d'une procédure stockée avec un objet de commande est généralement plus efficace pour réaliser des mises à jour, ainsi que d'autres opérations, car une procédure stockée ne nécessite pas la création d'un curseur. Pour en savoir plus sur les curseurs, reportez-vous au [Chapitre 8 : Présentation des curseurs et des verrous](chapter-8-understanding-cursors-and-locks.md).

