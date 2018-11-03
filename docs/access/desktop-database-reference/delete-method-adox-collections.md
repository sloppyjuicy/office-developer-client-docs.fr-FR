---
title: DELETE, méthode (Collections ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a429c18890125f1c047c6356d250713ea5ea817
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944899"
---
# <a name="delete-method-adox-collections"></a>DELETE, méthode (Collections ADOX)


**S’applique à**: Access 2013, Office 2013



Supprime un objet d'une collection.

## <a name="syntax"></a>Syntaxe

La *collection*. Supprimer le*nom*

## <a name="parameters"></a>Paramètres

- *Name*

  - Valeur de type **Variant** qui spécifie le nom ou la position ordinale (index) de l'objet à supprimer.

## <a name="remarks"></a>Notes

Une erreur se produit si le *nom* n’existe pas dans la collection.

Pour les collections [Tables](tables-collection-adox.md) et [Users](users-collection-adox.md), une erreur se produit si le fournisseur ne prend pas en charge la suppression respective des tables ou des utilisateurs. Pour les collections [Procedures](procedures-collection-adox.md) et [Views](views-collection-adox.md), la méthode **Delete** échoue si le fournisseur ne prend pas en charge les commandes persistantes.

