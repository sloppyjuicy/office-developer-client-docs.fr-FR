---
title: LogEvent, action de macro
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa036f73dd4c811191c9d5ba83a6d2fc65a54827
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918974"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="0e004-102">LogEvent, action de macro</span><span class="sxs-lookup"><span data-stu-id="0e004-102">LogEvent macro action</span></span>


<span data-ttu-id="0e004-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e004-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e004-104">L'action **ConsignerÉvénement** écrit des informations dans la table système **USysApplicationLog**.</span><span class="sxs-lookup"><span data-stu-id="0e004-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0e004-105">[!REMARQUE] L'action <STRONG>USysApplicationLog</STRONG> est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="0e004-105">The <STRONG>LogEvent</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="0e004-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0e004-106">Setting</span></span>

<span data-ttu-id="0e004-107">L'action **ConsignerÉvénement** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="0e004-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e004-108">Argument</span><span class="sxs-lookup"><span data-stu-id="0e004-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0e004-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0e004-109">Required</span></span></p></th>
<th><p><span data-ttu-id="0e004-110">Description</span><span class="sxs-lookup"><span data-stu-id="0e004-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e004-111"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="0e004-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="0e004-112">Non</span><span class="sxs-lookup"><span data-stu-id="0e004-112">No</span></span></p></td>
<td><p><span data-ttu-id="0e004-p101">Expression de type Chaîne qui décrit la condition que vous souhaitez consigner. La description ne doit pas dépasser 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="0e004-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e004-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0e004-115">Remarks</span></span>

<span data-ttu-id="0e004-p102">L'action **ConsignerÉvénement** peut être utilisée pour écrire des informations d'état dans la table système **USysApplicationLog** qui ne méritent pas l'utilisation de l'action **[DéclencherErreur](raiseerror-macro-action.md)** pour lever une erreur. Par exemple, vous pouvez consigner les modifications apportées à un champ spécifique ou utiliser les éléments écrits dans **USysApplicationLog** pour vous aider à déboguer votre macro.</span><span class="sxs-lookup"><span data-stu-id="0e004-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="0e004-118">Lorsque vous utilisez l'action **ConsignerÉvénement** pour écrire dans la table **USysApplicationLog**, la colonne **Catégorie** prend automatiquement la valeur **Utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="0e004-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="0e004-119">Pour afficher la table **USysApplicationLog**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0e004-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="0e004-120">Cliquez sur le menu **Fichier**, puis cliquez sur **Options**.</span><span class="sxs-lookup"><span data-stu-id="0e004-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="0e004-121">Dans la boîte dialogue **Options Access**, cliquez sur l'onglet **Base de données active**.</span><span class="sxs-lookup"><span data-stu-id="0e004-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="0e004-122">Dans la section **Navigation**, cliquez sur **Options de navigation**.</span><span class="sxs-lookup"><span data-stu-id="0e004-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="0e004-123">Dans la boîte de dialogue **Options de navigation**, cliquez sur **Afficher les objets système**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e004-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="0e004-124">Cliquez sur **OK** pour fermer la boîte de dialogue **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="0e004-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

