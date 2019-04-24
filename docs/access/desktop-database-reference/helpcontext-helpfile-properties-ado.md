---
title: HelpContext, HelpFile, propriétés (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291991"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="e30da-102">HelpContext, HelpFile, propriétés (ADO)</span><span class="sxs-lookup"><span data-stu-id="e30da-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="e30da-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e30da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e30da-104">Indique le fichier d'aide et la rubrique associés à un objet [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e30da-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="e30da-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e30da-105">Return values</span></span>

- <span data-ttu-id="e30da-106">**HelpContextID**: renvoie un ID de contexte pour une rubrique de fichier d'aide sous forme de valeur **Long**.</span><span class="sxs-lookup"><span data-stu-id="e30da-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="e30da-107">**HelpFile** : renvoie une valeur **String** qui correspond à un chemin d'accès à un fichier d'aide entièrement résolu.</span><span class="sxs-lookup"><span data-stu-id="e30da-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="e30da-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e30da-108">Remarks</span></span>

<span data-ttu-id="e30da-p101">Si un fichier d'aide est spécifié dans la propriété **HelpFile**, la propriété **HelpContext** permet d'afficher automatiquement la rubrique d'aide qu'elle identifie. Si aucune rubrique d'aide pertinente n'est disponible, la propriété **HelpContext** renvoie zéro et la propriété **HelpFile** renvoie une chaîne vide («   »).</span><span class="sxs-lookup"><span data-stu-id="e30da-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

