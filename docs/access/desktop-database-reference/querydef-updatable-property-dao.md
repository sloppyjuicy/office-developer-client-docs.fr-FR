---
title: Propriété QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0c1a85029270641a944d822ee81954ca1f2528e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919807"
---
# <a name="querydefupdatable-property-dao"></a>Propriété QueryDef.Updatable (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Mise à jour

*expression* Variable qui représente un objet **QueryDef** .

## <a name="remarks"></a>Remarques

La propriété **Updatable** d'un objet **QueryDef** a la valeur **True** si la définition de la requête peut être mise à jour même si l'objet **[Recordset](recordset-object-dao.md)** résultat n'est pas modifiable.

