---
title: Utilisation de la méthode AddNew en mode de mise à jour immédiate et par lot
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312753"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Utilisation de AddNew en mode Immédiat et Batch


**S’applique à** : Access 2013, Office 2013

Le comportement de la méthode **AddNew** varie en fonction du mode de mise à jour de l'objet **Recordset** et selon que vous passez ou non des arguments *FieldList* et *Values*.

En mode de mise à jour immédiate (où le fournisseur écrit les modifications dans la source de données sous-jacente dès que vous appelez la méthode **Update**), l'appel de la méthode **AddNew** sans argument affecte à la propriété **EditMode** la valeur **adEditAdd.** Le fournisseur met toutes les modifications des valeurs de champ dans un cache local. L'appel de la méthode **Update** publie le nouvel enregistrement dans la base de données et modifie la propriété **EditMode** en lui affectant la valeur **adEditNone**. Si vous passez les arguments *FieldList* et *Values*, ADO publie immédiatement le nouvel enregistrement dans la base de données (il n'est pas nécessaire d'appeler **Update**) et la valeur de la propriété **EditMode** ne change pas (**adEditNone**).

En mode de mise à jour par lot, l’appel de la méthode **AddNew** sans argument affecte à la propriété **EditMode** la valeur **adEditAdd**. Le fournisseur met toutes les modifications des valeurs de champ dans le cache local. L’appel de la méthode **Update** ajoute le nouvel enregistrement à l’objet **Recordset** actif et modifie la propriété **EditMode** en lui affectant la valeur **adEditNone**. En revanche, le fournisseur ne publie pas les modifications dans la base de données sous-jacente tant que vous n’avez appelé la méthode **UpdateBatch**. Si vous passez les arguments *FieldList* et *Values*, ADO envoie le nouvel enregistrement au fournisseur pour qu’il le stocke dans un cache ; vous devez appeler la méthode **UpdateBatch** pour publier le nouvel enregistrement dans la base de données sous-jacente. Pour plus d’informations sur **Update** et **UpdateBatch**, consultez le [chapitre  5 : Mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).

