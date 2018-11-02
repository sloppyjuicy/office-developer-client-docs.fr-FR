---
title: Precision, propriété (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e64a7166b73c5fca1fa7f5e0b63fabeec715c52
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927499"
---
# <a name="precision-property-adox"></a>Precision, propriété (ADOX)


**S’applique à**: Access 2013, Office 2013

Indique la précision maximale de valeurs de données de la colonne.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur de type **Long** qui correspond à la précision maximale des valeurs de données de la colonne lorsque la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) est de type numérique. La propriété **Precision** est ignorée pour tous les autres types de données.

## <a name="remarks"></a>Notes

La valeur par défaut est zéro (0).

Cette propriété est en lecture seule pour des objets [Column](column-object-adox.md) déjà ajoutés à une collection.

