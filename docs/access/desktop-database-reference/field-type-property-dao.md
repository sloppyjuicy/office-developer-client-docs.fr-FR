---
title: Field.Type, propriété (DAO)
TOCTitle: Type Property
description: Type, propriété
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 082f6b34965ae90c99efd8d8cf3ac34d2cfc5dfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581293"
---
# <a name="fieldtype-property-dao"></a>Field.Type, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. **Integer** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* .Type

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est une constante qui indique un type opérationnel ou de données. Pour un objet **Field**, cette propriété est en lecture/écriture jusqu'à ce que l'objet soit ajouté à une collection ou à un autre objet ; elle passe alors en lecture seule.

Pour un objet **Field**, les valeurs des paramètres et de retour possibles sont décrits dans le tableau suivant.

|**Constante**|**Valeur**|**Description**|
|:----------|:----------|:----------|
|**dbBigInt**|16|Entier très grand|
|**dbBinary**|9|Binary|
|**dbBoolean**|1|Valeur booléenne|
|**dbByte**|2|Octet|
|**dbChar**|18|Char|
|**dbCurrency**|5|Devise|
|**dbDate**|8|Date/Heure|
|**dbDecimal**|20|Décimal|
|**dbDouble**|7|Double|
|**dbFloat**|21|Flottant|
|**dbGUID**|15|GUID|
|**dbInteger**|3|Entier|
|**dbLong**|4|Entier long|
|**dbLongBinary**|11|Binaire long (objet OLE)|
|**dbMemo**|12|Mémo|
|**dbNumeric**|19|Numérique|
|**dbSingle**|6|Unique|
|**dbText**|10|Text|
|**dbTime**|22|Time|
|**dbTimeStamp**|23|Date et heure|
|**dbVarBinary**|17|VarBinary|

Lorsque vous ajoutez un nouvel objet **Field**, **Parameter** ou **Property** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** ou **TableDef**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié pour le nouvel objet.
