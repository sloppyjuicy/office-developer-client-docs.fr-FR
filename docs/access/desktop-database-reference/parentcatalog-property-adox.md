---
title: ParentCatalog, propriété (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 644312ab6b51b1b084d2d11f52117cece7afdf0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469587"
---
# <a name="parentcatalog-property-adox"></a>ParentCatalog, propriété (ADOX)


**S’applique à**: Access 2013 | Office 2013

Spécifie le catalogue parent d'une table ou colonne afin de fournir l'accès à des propriétés spécifiques au fournisseur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie un objet [Catalog](catalog-object-adox.md). En affectant à **ParentCatalog** un objet **Catalog** ouvert, vous pouvez accéder aux propriétés spécifiques à un fournisseur avant d'ajouter une table ou une colonne à une collection **Catalog**.

## <a name="remarks"></a>Notes

Certains fournisseurs de données permettent uniquement d'écrire des valeurs de propriétés qui leur sont spécifiques lors de la création (lorsque vous ajoutez une table ou une colonne à sa collection **Catalog** ). Pour accéder à ces propriétés avant d'ajouter ces objets à un objet **Catalog**, spécifiez d'abord l'objet **Catalog** dans la propriété **ParentCatalog**.

Une erreur se produit lorsque la table ou la colonne est ajoutée à un objet **Catalog** différent de celui spécifié dans la propriété **ParentCatalog**.

