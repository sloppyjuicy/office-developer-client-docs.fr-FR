---
title: OpenDiagram, action de macro
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719623"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="d5f4f-102">OpenDiagram, action de macro</span><span class="sxs-lookup"><span data-stu-id="d5f4f-102">OpenDiagram macro action</span></span>

<span data-ttu-id="d5f4f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5f4f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5f4f-104">Dans un projet Access, vous pouvez utiliser l'action **OuvrirSchéma** pour ouvrir un schéma de base de données en mode Création.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="d5f4f-105">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="d5f4f-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d5f4f-106">Setting</span></span>

<span data-ttu-id="d5f4f-107">L'action **OuvrirSchéma** possède l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-107">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5f4f-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d5f4f-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d5f4f-109">Description</span><span class="sxs-lookup"><span data-stu-id="d5f4f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f4f-110"><strong>Nom du schéma</strong></span><span class="sxs-lookup"><span data-stu-id="d5f4f-110"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f4f-111">Le nom du schéma de base de données à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-111">The name of the database diagram to open.</span></span> <span data-ttu-id="d5f4f-112">La zone <strong>Nom du schéma</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche tous les schémas de base de données dans la base de données en cours.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-112">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="d5f4f-113">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-113">This is a required argument.</span></span> <span data-ttu-id="d5f4f-114">Si vous exécutez une macro contenant l’action <strong>OuvrirSchéma</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord le schéma portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-114">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="d5f4f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d5f4f-115">Remarks</span></span>

<span data-ttu-id="d5f4f-116">Cette action équivaut à double-cliquer sur un schéma de base de données dans le volet de navigation ou à cliquer avec le bouton droit sur le schéma de base de données dans le volet de navigation, puis à cliquer sur **Mode Création**.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-116">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>

> [!TIP]
> <span data-ttu-id="d5f4f-p102">[!CONSEIL] Vous pouvez faire glisser un schéma de base de données depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action **OuvrirSchéma** qui ouvre le schéma de base de données en mode Création.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-p102">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span></span>

<span data-ttu-id="d5f4f-119">Pour exécuter l'action **OuvrirSchéma** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenDiagram** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

