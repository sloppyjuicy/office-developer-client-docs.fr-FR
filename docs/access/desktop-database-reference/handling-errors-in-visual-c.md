---
title: Gestion des erreurs dans Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bb499b24b151f93d68ef28594217f6707bb48b34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615444"
---
# <a name="handling-errors-in-visual-c"></a>Gestion des erreurs dans Visual C++


**S’applique à** : Access 2013, Office 2013

Dans COM, la plupart des opérations renvoient un code de retour HRESULT qui indique si une fonction a été correctement exécutée. La directive d’importation génère du code de wrapper autour de chaque méthode ou propriété « brute » et vérifie \# le HRESULT renvoyé. Si HRESULT indique un échec, le code wrapper envoie une erreur COM en appelant \_ com \_ issue errorex() avec le code de retour \_ HRESULT comme argument. Vous pouvez intercepter les objets d'erreurs COM dans un bloc **try-catch**. (Pour plus d’efficacité, capturez une référence à un objet \_ \_ d’erreur com.)

N'oubliez pas qu'il s'agit d'erreurs ADO : elles résultent de l'échec d'une opération ADO. Les erreurs renvoyées par le fournisseur sous-jacent apparaissent en tant qu'objets **Error** dans la collection **Errors** de l'objet **Connection**.

La directive d’importation crée uniquement des routines de gestion des erreurs pour les méthodes et propriétés déclarées dans le .dll \# ADO. Toutefois, vous pouvez bénéficier de ce même mécanisme de gestion des erreurs en écrivant votre propre macro ou fonction en ligne de vérification des erreurs. Reportez-vous à la rubrique Extensions Visual C++ pour obtenir des exemples.

