---
title: Gestion des erreurs dans Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99f8a0f8c7b79769fba62b38ef5517781aea4600
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945606"
---
# <a name="handling-errors-in-visual-c"></a>Gestion des erreurs dans Visual C++


**S’applique à**: Access 2013, Office 2013

Dans COM, la plupart des opérations renvoient un code de retour HRESULT qui indique si une fonction a été correctement exécutée. Le \#directive import génère un code wrapper pour chaque méthode « brute » ou la propriété et vérifie le HRESULT renvoyé. Si HRESULT indique un échec, le code de wrapper génère une erreur COM en appelant \_com\_problème\_errorex() avec HRESULT retourner le code en tant qu’argument. Vous pouvez intercepter les objets d'erreurs COM dans un bloc **try-catch**. (Par souci d’efficacité, interceptez une référence à un \_com\_objet error.)

N'oubliez pas qu'il s'agit d'erreurs ADO : elles résultent de l'échec d'une opération ADO. Les erreurs renvoyées par le fournisseur sous-jacent apparaissent en tant qu'objets **Error** dans la collection **Errors** de l'objet **Connection**.

Le \#directive import ne crée des routines de gestion des erreurs pour les méthodes et propriétés déclarées dans le fichier .dll ADO. Toutefois, vous pouvez bénéficier de ce même mécanisme de gestion des erreurs en écrivant votre propre macro ou fonction en ligne de vérification des erreurs. Reportez-vous à la rubrique Extensions Visual C++ pour obtenir des exemples.

