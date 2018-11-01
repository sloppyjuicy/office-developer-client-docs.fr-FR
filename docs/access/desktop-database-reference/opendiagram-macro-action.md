---
title: OuvrirSchéma, action de macro
TOCTitle: OpenDiagram Macro Action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3118c2a6b85d400b4b797c4b9b711e5f5a512c62
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869238"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="3c86c-102">OuvrirSchéma, action de macro</span><span class="sxs-lookup"><span data-stu-id="3c86c-102">OpenDiagram Macro Action</span></span>


<span data-ttu-id="3c86c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c86c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c86c-104">Dans un projet Access, vous pouvez utiliser l'action **OuvrirSchéma** pour ouvrir un schéma de base de données en mode Création.</span><span class="sxs-lookup"><span data-stu-id="3c86c-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3c86c-p101">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="3c86c-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="3c86c-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3c86c-107">Setting</span></span>

<span data-ttu-id="3c86c-108">L'action **OuvrirSchéma** possède l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="3c86c-108">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c86c-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="3c86c-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3c86c-110">Description</span><span class="sxs-lookup"><span data-stu-id="3c86c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c86c-111"><strong>Nom du schéma</strong></span><span class="sxs-lookup"><span data-stu-id="3c86c-111"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3c86c-112">Le nom du schéma de base de données à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="3c86c-112">The name of the database diagram to open.</span></span> <span data-ttu-id="3c86c-113">La zone <strong>Nom du schéma</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche tous les schémas de base de données dans la base de données en cours.</span><span class="sxs-lookup"><span data-stu-id="3c86c-113">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="3c86c-114">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3c86c-114">This is a required argument.</span></span> <span data-ttu-id="3c86c-115">Si vous exécutez une macro contenant l’action <strong>OuvrirSchéma</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord le schéma portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="3c86c-115">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3c86c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3c86c-116">Remarks</span></span>

<span data-ttu-id="3c86c-117">Cette action équivaut à double-cliquer sur un schéma de base de données dans le volet de navigation ou à cliquer avec le bouton droit sur le schéma de base de données dans le volet de navigation, puis à cliquer sur **Mode Création**.</span><span class="sxs-lookup"><span data-stu-id="3c86c-117">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>


> [!TIP]
> <P><span data-ttu-id="3c86c-p103">[!CONSEIL] Vous pouvez faire glisser un schéma de base de données depuis le volet de navigation vers une ligne d'action de macro. Ceci crée automatiquement une action <STRONG>OuvrirSchéma</STRONG> qui ouvre le schéma de base de données en mode Création.</span><span class="sxs-lookup"><span data-stu-id="3c86c-p103">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an <STRONG>OpenDiagram</STRONG> action that opens the database diagram in Design view.</span></span></P>



<span data-ttu-id="3c86c-120">Pour exécuter l'action **OuvrirSchéma** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **OpenDiagram** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="3c86c-120">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

