---
title: Utilisation de la méthode AddNew en mode de mise à jour immédiate et par lot
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79bd4ed656da49e61ea70ace3b11f09c19382b03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943639"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Avec la méthode AddNew en mode exécution et par lot


**S’applique à**: Access 2013, Office 2013

Le comportement de la méthode **AddNew** varie selon le mode de mise à jour de l’objet **Recordset** et selon que vous passez les arguments *FieldList* et *Values* .

En mode de mise à jour immédiate (où le fournisseur écrit les modifications dans la source de données sous-jacente dès que vous appelez la méthode **Update**), l'appel de la méthode **AddNew** sans argument affecte à la propriété **EditMode** la valeur **adEditAdd.** Le fournisseur met toutes les modifications des valeurs de champ dans un cache local. L'appel de la méthode **Update** publie le nouvel enregistrement dans la base de données et modifie la propriété **EditMode** en lui affectant la valeur **adEditNone**. Si vous passez les arguments *FieldList* et *Values*, ADO publie immédiatement le nouvel enregistrement dans la base de données (il n'est pas nécessaire d'appeler **Update**) et la valeur de la propriété **EditMode** ne change pas (**adEditNone**).

En mode de mise à jour par lot, l’appel de la méthode **AddNew** sans arguments définit la propriété **EditMode** à **adEditAdd**. Le fournisseur met en cache toutes les modifications locales de valeurs de champ. Appeler la méthode **Update** ajoute le nouvel enregistrement au **Recordset** actif et réinitialise la propriété **EditMode** à **adEditNone**, mais le fournisseur ne valide pas les modifications apportées à la base de données sous-jacente que lorsque vous appelez la méthode UpdateBatch ** **méthode. Si vous passez des arguments *FieldList* et *Values* , ADO envoie le nouvel enregistrement au fournisseur pour le stockage dans un cache ; Vous devez appeler la méthode **UpdateBatch** pour publier le nouvel enregistrement dans la base de données sous-jacente. Pour plus d’informations sur la **mise à jour** et **UpdateBatch**, voir [chapitre 5 : mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).

