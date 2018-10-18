---
title: Source, propriété (objet Recordset ADO)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605260"
---
# <a name="source-property-ado-recordset"></a>Source, propriété (objet Recordset ADO)


**S’applique à**: Access 2013 | Office 2013

Indique la source de données d'un objet [Recordset](recordset-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit une valeur **String** ou une référence à un objet [Command](command-object-ado.md) ; renvoie uniquement une valeur **String** qui indique la source du **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Source** pour spécifier la source de données d'un objet **Recordset** en utilisant l'une des options suivantes : une variable d'objet **Command**, une instruction SQL, une procédure stockée ou le nom d'une table.

Si vous définissez que la propriété **Source** est un objet **Command**, la propriété [ActiveConnection](activeconnection-property-ado.md) de l'objet **Recordset** hérite sa valeur de la propriété **ActiveConnection** de l'objet **Command** spécifié. Toutefois, la lecture de la propriété **Source** ne renvoie pas un objet **Command**, mais la propriété [CommandText](commandtext-property-ado.md) de l'objet **Command** pour lequel vous avez défini la propriété **Source**.

Si la propriété **Source** est une instruction SQL, une procédure stockée ou un nom de table, vous pouvez optimiser les performances en passant l’argument *Options* approprié avec l’appel de la méthode [Open](open-method-ado-recordset.md) .

La propriété **Source** est en lecture/écriture pour les objets **Recordset** fermés et lecture seule pour les objets **Recordset** ouverts.

