---
title: Méthode Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81b08472b46ab3a3d35d184e2f8b7be8673f7d1f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927262"
---
# <a name="recordsetcancel-method-dao"></a>Méthode Recordset.Cancel (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . Annuler

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Utilisez la méthode **Cancel** pour mettre fin à l’exécution d’un appel de méthode **Execute** ou **OpenConnection** asynchrone (autrement dit, la méthode a été appelée avec l’option dbRunAsync). **Annuler** renvoie une erreur d’exécution si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez d’interrompre.

