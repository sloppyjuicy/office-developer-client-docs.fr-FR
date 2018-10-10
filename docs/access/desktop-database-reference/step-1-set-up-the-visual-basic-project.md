---
title: 'Étape 1 : configurer le projet Visual Basic'
TOCTitle: 'Step 1: Set Up the Visual Basic Project'
ms:assetid: 1b8195c9-60c8-18a2-3fa2-ffdeed370748
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248954(v=office.15)
ms:contentKeyID: 48543544
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f608d0dadb44a6ddea7a60123d2d6950bc9627cb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469953"
---
# <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="e5bf1-102">Étape 1 : configurer le projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e5bf1-102">Step 1: Set Up the Visual Basic Project</span></span>


<span data-ttu-id="e5bf1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5bf1-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="e5bf1-104">Étape 1 : configurer le projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e5bf1-104">Step 1: Set Up the Visual Basic Project</span></span>

<span data-ttu-id="e5bf1-105">Dans ce scénario, vous êtes censé avoir installé sur votre système Microsoft Visual Basic version 6.0 ou ultérieure, ADO version 2.5 ou ultérieure, et le fournisseur Microsoft OLE DB pour la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-105">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

<span data-ttu-id="e5bf1-106">**Pour créer un projet ADO**</span><span class="sxs-lookup"><span data-stu-id="e5bf1-106">**To create an ADO project**</span></span>

1.  <span data-ttu-id="e5bf1-107">Dans Microsoft Visual Basic, créez un nouveau projet EXE standard.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-107">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="e5bf1-108">Dans le menu **Projet**, choisissez **Références**.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-108">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="e5bf1-109">Sélectionnez **" Microsoft ActiveX Data Objects 2.5**" et cliquez sur**OK**.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-109">Select **"Microsoft ActiveX Data Objects 2.5 Library**" and click **OK**.</span></span>

<span data-ttu-id="e5bf1-110">**Pour insérer des contrôles dans le formulaire principal**</span><span class="sxs-lookup"><span data-stu-id="e5bf1-110">**To insert controls on the main form**</span></span>

1.  <span data-ttu-id="e5bf1-p101">Ajoutez un contrôle ListBox à Form1. Attribuez à sa propriété **Name** la valeur lstMain.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-p101">Add a ListBox control to Form1. Set its **Name** property to lstMain.</span></span>

2.  <span data-ttu-id="e5bf1-p102">Ajoutez un autre contrôle ListBox à Form1. Attribuez à sa propriété **Name** la valeur lstDetails.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-p102">Add another ListBox control to Form1. Set its **Name** property to lstDetails.</span></span>

3.  <span data-ttu-id="e5bf1-p103">Ajoutez un contrôle TextBox à Form1. Attribuez à sa propriété **Name** la valeur txtDetails.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-p103">Add a TextBox control to Form1. Set its **Name** property to txtDetails.</span></span>

