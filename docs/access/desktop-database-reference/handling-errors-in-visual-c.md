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
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="df64a-102">Gestion des erreurs dans Visual C++</span><span class="sxs-lookup"><span data-stu-id="df64a-102">Handling errors in Visual C++</span></span>


<span data-ttu-id="df64a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df64a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df64a-104">Dans COM, la plupart des opérations renvoient un code de retour HRESULT qui indique si une fonction a été correctement exécutée.</span><span class="sxs-lookup"><span data-stu-id="df64a-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="df64a-105">Le \#directive import génère un code wrapper pour chaque méthode « brute » ou la propriété et vérifie le HRESULT renvoyé.</span><span class="sxs-lookup"><span data-stu-id="df64a-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="df64a-106">Si HRESULT indique un échec, le code de wrapper génère une erreur COM en appelant \_com\_problème\_errorex() avec HRESULT retourner le code en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="df64a-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="df64a-107">Vous pouvez intercepter les objets d'erreurs COM dans un bloc **try-catch**.</span><span class="sxs-lookup"><span data-stu-id="df64a-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="df64a-108">(Par souci d’efficacité, interceptez une référence à un \_com\_objet error.)</span><span class="sxs-lookup"><span data-stu-id="df64a-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="df64a-p102">N'oubliez pas qu'il s'agit d'erreurs ADO : elles résultent de l'échec d'une opération ADO. Les erreurs renvoyées par le fournisseur sous-jacent apparaissent en tant qu'objets **Error** dans la collection **Errors** de l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="df64a-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="df64a-111">Le \#directive import ne crée des routines de gestion des erreurs pour les méthodes et propriétés déclarées dans le fichier .dll ADO.</span><span class="sxs-lookup"><span data-stu-id="df64a-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="df64a-112">Toutefois, vous pouvez bénéficier de ce même mécanisme de gestion des erreurs en écrivant votre propre macro ou fonction en ligne de vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="df64a-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="df64a-113">Reportez-vous à la rubrique Extensions Visual C++ pour obtenir des exemples.</span><span class="sxs-lookup"><span data-stu-id="df64a-113">See the topic Visual C++ Extensions for examples.</span></span>

