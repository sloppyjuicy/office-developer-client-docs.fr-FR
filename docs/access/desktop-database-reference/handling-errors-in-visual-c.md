---
title: Gestion des erreurs dans Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709473"
---
# <a name="handling-errors-in-visual-c"></a>Gestion des erreurs dans Visual C++


**S’applique à**: Access 2013, Office 2013

Dans COM, la plupart des opérations renvoient un code de retour HRESULT qui indique si une fonction a été correctement exécutée. Le \#directive import génère un code wrapper pour chaque méthode « brute » ou la propriété et vérifie le HRESULT renvoyé. Si HRESULT indique un échec, le code de wrapper génère une erreur COM en appelant \_com\_problème\_errorex() avec HRESULT retourner le code en tant qu’argument. Vous pouvez intercepter les objets d'erreurs COM dans un bloc **try-catch**. (Par souci d’efficacité, interceptez une référence à un \_com\_objet error.)

N'oubliez pas qu'il s'agit d'erreurs ADO : elles résultent de l'échec d'une opération ADO. Les erreurs renvoyées par le fournisseur sous-jacent apparaissent en tant qu'objets **Error** dans la collection **Errors** de l'objet **Connection**.

Le \#directive import ne crée des routines de gestion des erreurs pour les méthodes et propriétés déclarées dans le fichier .dll ADO. Toutefois, vous pouvez bénéficier de ce même mécanisme de gestion des erreurs en écrivant votre propre macro ou fonction en ligne de vérification des erreurs. Reportez-vous à la rubrique Extensions Visual C++ pour obtenir des exemples.

