---
title: Propriété Parameter.Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95086e811288bd70dce15a22319531b28a1ecd6c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996726"
---
# <a name="parametervalue-property-dao"></a>Propriété Parameter.Value (DAO)

**S’applique à**: Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. Type de données **Variant** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Valeur

*expression* Variable qui représente un objet **Parameter** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données Variant qui est évalué à une valeur appropriée pour le type de données, tel que spécifié par la propriété **Type** d'un objet.

En général, la propriété **Value** est utilisée pour récupérer et modifier les données dans les objets **Recordset**.

La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.

Si vous essayez de définir ou de renvoyer la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), vous obtenez une erreur interceptable.

> [!NOTE]
> Lorsque vous lisez des valeurs décimales depuis une base de données Microsoft SQL Server, elle sont mises en forme à l'aide d'une notation scientifique via un espace de travail Microsoft Access, mais elles s'affichent sous forme de valeurs décimales normales via un espace de travail ODBCDirect.


