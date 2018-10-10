---
title: TableDef.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b39f263786dafd23234747f72f5e289a2350e1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469092"
---
# <a name="tabledefvalidationtext-property-dao"></a>TableDef.ValidationText Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet **Field** n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété **ValidationRule** (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . ValidationText (MessageSiErreur)

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

Pour un objet **[TableDef](tabledef-object-dao.md)**, cette propriété est en lecture seule pour une table liée et en lecture/écriture pour une table de base.

