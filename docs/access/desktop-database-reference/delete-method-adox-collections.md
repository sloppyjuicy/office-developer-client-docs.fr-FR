---
title: Delete, méthode (collections ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294077"
---
# <a name="delete-method-adox-collections"></a>Delete, méthode (collections ADOX)

**S’applique à** : Access 2013, Office 2013

Supprime un objet d'une collection.

## <a name="syntax"></a>Syntaxe

*Collection*. Supprimer le*nom*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*Name* |Valeur de type **Variant** qui spécifie le nom ou la position ordinale (index) de l'objet à supprimer.|

## <a name="remarks"></a>Remarques

Une erreur se produit si le paramètre *Name* n'existe pas dans la collection.

Pour les collections [Tables](tables-collection-adox.md) et [Users](users-collection-adox.md), une erreur se produit si le fournisseur ne prend pas en charge la suppression respective des tables ou des utilisateurs. Pour les collections [Procedures](procedures-collection-adox.md) et [Views](views-collection-adox.md), la méthode **Delete** échoue si le fournisseur ne prend pas en charge les commandes persistantes.

