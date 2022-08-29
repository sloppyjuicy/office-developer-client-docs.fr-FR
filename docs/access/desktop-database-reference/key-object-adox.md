---
title: Key Object (ADOX - Informations de référence sur la base de données de bureau Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d0915366cee814953921962ec8de3d7de1eda1d3
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365480"
---
# <a name="key-object-adox"></a>Objet Key (ADOX)


**S’applique à** : Access 2013, Office 2013

Représente un champ de clé primaire, étrangère ou unique d'une table de base de données.

## <a name="remarks"></a>Remarques

Le code suivant permet de créer une nouvelle **clé** :

`Dim obj As New Key`

Avec les propriétés et collections d'un objet **Key**, vous pouvez :

- Identifier la clé à l'aide de la propriété [Name](name-property-adox.md).

- Déterminer si la clé est primaire, étrangère ou unique à l'aide de la propriété [Type](/office/vba/access/concepts/miscellaneous/type-property-keyadox).

- Accéder aux colonnes de base de données de la clé à l'aide de la collection [Columns](columns-collection-adox.md).

- Spécifier le nom de la table connexe à l'aide de la propriété [RelatedTable](relatedtable-property-adox.md).

- Déterminer l'opération effectuée lors de la suppression ou de la mise à jour d'une clé primaire à l'aide des propriétés [DeleteRule](deleterule-property-adox.md) et [UpdateRule](updaterule-property-adox.md).

