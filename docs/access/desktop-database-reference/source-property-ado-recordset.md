---
title: Source, propriété (objet Recordset ADO)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aa6ef3bb28fbd9a4c44d45f1e503ab14021c8b9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568403"
---
# <a name="source-property-ado-recordset"></a>Source, propriété (objet Recordset ADO)


**S’applique à** : Access 2013, Office 2013

Indique la source de données d'un objet [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit une valeur **String** ou une référence à un objet [Command](command-object-ado.md) ; renvoie uniquement une valeur **String** qui indique la source du **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Source** pour spécifier la source de données d'un objet **Recordset** en utilisant l'une des options suivantes : une variable d'objet **Command**, une instruction SQL, une procédure stockée ou le nom d'une table.

Si vous définissez que la propriété **Source** est un objet **Command**, la propriété [ActiveConnection](activeconnection-property-ado.md) de l'objet **Recordset** hérite sa valeur de la propriété **ActiveConnection** de l'objet **Command** spécifié. Toutefois, la lecture de la propriété **Source** ne renvoie pas un objet **Command**, mais la propriété [CommandText](commandtext-property-ado.md) de l'objet **Command** pour lequel vous avez défini la propriété **Source**.

Si la propriété **Source** est une instruction SQL, une procédure stockée ou un nom de table, vous pouvez optimiser les performances en passant l’argument *Options* approprié avec l’appel de méthode [Open](open-method-ado-recordset.md).

La propriété **Source** est en lecture/écriture pour les objets **Recordset** fermés et lecture seule pour les objets **Recordset** ouverts.

