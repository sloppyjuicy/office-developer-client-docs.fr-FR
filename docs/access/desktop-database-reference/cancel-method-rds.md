---
title: Cancel, méthode (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35322ec058d31f92288fd06a4e8434a4256c2d74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720764"
---
# <a name="cancel-method-rds"></a>Cancel, méthode (RDS)


**S’applique à**: Access 2013, Office 2013

Annule l'exécution d'un appel de méthode asynchrone en attente.

## <a name="syntax"></a>Syntaxe

*RDS*. *DataControl*. Annuler

## <a name="remarks"></a>Notes

Lorsque vous appelez **Cancel**, [ReadyState](readystate-property-rds.md) prend automatiquement la valeur **adcReadyStateLoaded** et l'objet [Recordset](recordset-object-ado.md) sera vide.

