---
title: State, propriété (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306362"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="8291c-102">State, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8291c-102">State property (ADO MD)</span></span>


<span data-ttu-id="8291c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8291c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8291c-104">Indique l'état actuel de l'ensemble de cellules.</span><span class="sxs-lookup"><span data-stu-id="8291c-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="8291c-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="8291c-105">Return values</span></span>

<span data-ttu-id="8291c-106">Retourne un entier de type **Long** qui indique la condition actuelle de l'objet [Cellset](cellset-object-ado-md.md) et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8291c-106">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only.</span></span> <span data-ttu-id="8291c-107">Les valeurs suivantes sont valides :**adStateClosed** (0) et **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="8291c-107">The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="8291c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="8291c-108">Remarks</span></span>

<span data-ttu-id="8291c-p102">Pour utiliser les noms des constantes [ObjectStateEnum](objectstateenum.md)  la bibliothèque de types ADO doit être référencée dans votre projet. Pour plus d’informations, consultez  [Utilisation d’ADO avec ADO MD](using-ado-with-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="8291c-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

