---
title: ParentCatalog, propriété (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f48c7fa35095fab97352d6ce4cc47dd2cd1cf397
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585483"
---
# <a name="parentcatalog-property-adox"></a>ParentCatalog, propriété (ADOX)


**S’applique à** : Access 2013, Office 2013

Spécifie le catalogue parent d'une table ou colonne afin de fournir l'accès à des propriétés spécifiques au fournisseur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie un objet [Catalog](catalog-object-adox.md). En affectant à **ParentCatalog** un objet **Catalog** ouvert, vous pouvez accéder aux propriétés spécifiques à un fournisseur avant d'ajouter une table ou une colonne à une collection **Catalog**.

## <a name="remarks"></a>Remarques

Certains fournisseurs de données permettent uniquement d'écrire des valeurs de propriétés qui leur sont spécifiques lors de la création (lorsque vous ajoutez une table ou une colonne à sa collection **Catalog** ). Pour accéder à ces propriétés avant d'ajouter ces objets à un objet **Catalog**, spécifiez d'abord l'objet **Catalog** dans la propriété **ParentCatalog**.

Une erreur se produit lorsque la table ou la colonne est ajoutée à un objet **Catalog** différent de celui spécifié dans la propriété **ParentCatalog**.

