---
title: EndOfRecordset, événement (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89ca397c4e95dd6f18de41862e9383f77fe14aa8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928837"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset, événement (ADO)


**S’applique à**: Access 2013, Office 2013



L'événement **EndOfRecordset** est appelé lors d'une tentative de positionnement sur une ligne au-delà de la fin d'un objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

EndOfRecordset*fMoreData*, *adStatus*, *Connection*

## <a name="parameters"></a>Paramètres

  - *fMoreData*

  - A **VARIANT\_BOOL** valeur de la valeur de type VARIANT\_la valeur TRUE, indique plus de lignes qui ont été ajoutés au **jeu d’enregistrements**.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Lorsque **EndOfRecordset** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement et à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en question.
    
    Avant que **EndOfRecordset** ne soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre afin d'empêcher toute notification ultérieure.

  - *Connection*

  - Objet **Recordset**. Le **jeu d’enregistrements** pour laquelle cet événement se produit.

## <a name="remarks"></a>Notes

Un événement **EndOfRecordset** peut être généré si l'opération [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) échoue.

Ce gestionnaire d'événements est appelé lors d'une tentative de positionnement au-delà de la fin de l'objet **Recordset**, résultant probablement d'un appel à **MoveNext**. À partir de l'événement, il est toujours possible toutefois de récupérer plusieurs enregistrements d'une base de données et de les ajouter à la fin de l'objet **Recordset**. Dans ce cas, la valeur de type VARIANT *fMoreData* \_la valeur TRUE et de retour à partir de **l’événement EndOfRecordset**. Rappelez ensuite **MoveNext** pour accéder aux nouveaux enregistrements récupérés.

