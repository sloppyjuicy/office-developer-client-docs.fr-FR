---
title: Direction, propriété (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9e34522a69b2e79f8ef44b912e2c0648c5b813d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881292"
---
# <a name="direction-property-ado"></a>Direction, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique si l'objet [Parameter](parameter-object-ado.md) représente un paramètre d'entrée, de sortie, d'entrée et de sortie, ou encore si le paramètre est la valeur renvoyée par une procédure stockée.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur [ParameterDirectionEnum](parameterdirectionenum.md).

## <a name="remarks"></a>Notes

Utilisez la propriété **Direction** pour spécifier le mode de transmission d'un paramètre dans une procédure. La propriété **Direction** est en lecture-écriture, ce qui vous permet d'utiliser des fournisseurs qui ne retournent pas ces informations ou de définir ces informations lorsque vous ne souhaitez pas qu'ADO effectue un appel supplémentaire au fournisseur pour récupérer des informations de paramètre.

Les fournisseurs ne peuvent pas tous déterminer la direction des paramètres dans leurs procédures stockées. En pareil cas, vous devez définir la propriété **Direction** avant d'exécuter la requête.

