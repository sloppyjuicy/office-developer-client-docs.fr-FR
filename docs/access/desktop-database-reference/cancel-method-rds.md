---
title: Cancel, méthode (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afe7a01cf00cfc432757e7c6289d0e9eabc5bc0a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920122"
---
# <a name="cancel-method-rds"></a>Cancel, méthode (RDS)


**S’applique à**: Access 2013, Office 2013

Annule l'exécution d'un appel de méthode asynchrone en attente.

## <a name="syntax"></a>Syntaxe

*RDS*. *DataControl*. Annuler

## <a name="remarks"></a>Notes

Lorsque vous appelez **Cancel**, [ReadyState](readystate-property-rds.md) prend automatiquement la valeur **adcReadyStateLoaded** et l'objet [Recordset](recordset-object-ado.md) sera vide.

