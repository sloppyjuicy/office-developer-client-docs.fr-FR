---
title: Type, propriété (objet Stream ADO)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fdf3f40565f41a3d34b2202c4e079839af1f1ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602740"
---
# <a name="type-property-ado-stream"></a>Type, propriété (objet Stream ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le type de données contenu dans l'objet [Stream](stream-object-ado.md) (binaire ou texte).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur [StreamTypeEnum](streamtypeenum.md) qui spécifie le type de données contenu dans l'objet **Stream**. La valeur par défaut est **adTypeText**. Toutefois, si ce sont des données binaires qui sont initialement écrites dans un nouvel objet **Stream** vide, la valeur de la propriété **Type** devient **adTypeBinary**.

## <a name="remarks"></a>Remarques

La propriété **Type** n’est accessible en lecture et en écriture que lorsque la position actuelle est au début de l’objet **Stream** (la valeur de la propriété [Position](position-property-ado.md) est 0) ; elle est en lecture seule pour toute autre position.

La propriété **Type** détermine les méthodes devant être utilisées pour effectuer des lectures et des écritures sur l'objet **Stream**. Pour les objets **Stream** textuels, utilisez [ReadText](readtext-method-ado.md) et [Writetext](writetext-method-ado.md). Pour les objets **Stream** binaires, utilisez [Read](read-method-ado.md) et [Write](write-method-ado.md).

