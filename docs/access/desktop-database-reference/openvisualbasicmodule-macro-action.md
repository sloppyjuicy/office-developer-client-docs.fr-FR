---
title: OuvrirModuleVisualBasic, action de macro
TOCTitle: OpenVisualBasicModule Macro Action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bfb2238bf81215acef7026bb878dca9d1dbceb61
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869882"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="66bab-102">OuvrirModuleVisualBasic, action de macro</span><span class="sxs-lookup"><span data-stu-id="66bab-102">OpenVisualBasicModule Macro Action</span></span>


<span data-ttu-id="66bab-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66bab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66bab-p101">Utilisez l'action **OuvrirModuleVisualBasic** pour ouvrir un module Visual Basic pour Applications (VBA) spécifique à une certaine procédure. Il peut s'agir d'une procédure Sub, d'une procédure Function ou d'une procédure événementielle.</span><span class="sxs-lookup"><span data-stu-id="66bab-p101">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>


> [!NOTE]
> <P><span data-ttu-id="66bab-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="66bab-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="66bab-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="66bab-108">Setting</span></span>

<span data-ttu-id="66bab-109">L'action **OuvrirModuleVisualBasic** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="66bab-109">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66bab-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="66bab-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="66bab-111">Description</span><span class="sxs-lookup"><span data-stu-id="66bab-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66bab-112"><strong>Nom du module</strong></span><span class="sxs-lookup"><span data-stu-id="66bab-112"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="66bab-113">Le nom du module que vous souhaitez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="66bab-113">The name of the module you want to open.</span></span> <span data-ttu-id="66bab-114">Vous pouvez laisser cet argument vide si vous souhaitez rechercher tous les modules standard dans la base de données pour une procédure et ouvrez le module approprié dans cette procédure.</span><span class="sxs-lookup"><span data-stu-id="66bab-114">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="66bab-115">Si vous exécutez une macro contenant l’action <strong>OuvrirModuleVisualBasic</strong> dans une base de données bibliothèque, Microsoft Access recherche d’abord le module portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="66bab-115">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66bab-116"><strong>Nom de la procédure</strong></span><span class="sxs-lookup"><span data-stu-id="66bab-116"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="66bab-p104">Nom de la procédure dans laquelle vous voulez ouvrir le module. Si vous laissez cet argument vierge, le module s’ouvre sur la section Déclarations.</span><span class="sxs-lookup"><span data-stu-id="66bab-p104">The name of the procedure you want to open the module to. If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="66bab-119">[!REMARQUE] Vous devez entrer un nom valide dans l'argument <STRONG>Nom du module</STRONG> ou <STRONG>Nom de la procédure</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="66bab-119">You must enter a valid name in either the <STRONG>Module Name</STRONG> or <STRONG>Procedure Name</STRONG> argument.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="66bab-120">Notes</span><span class="sxs-lookup"><span data-stu-id="66bab-120">Remarks</span></span>

<span data-ttu-id="66bab-121">Vous pouvez utiliser cette action pour ouvrir une procédure événementielle en spécifiant les arguments **Nom du module** et **Nom de la procédure**.</span><span class="sxs-lookup"><span data-stu-id="66bab-121">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="66bab-122">Par exemple, pour ouvrir la procédure d’événement **Click** du bouton ImpressionFacture du formulaire commandes, définissez l’argument **Nom du Module** sur **formulaire.commandes** et définissez l’argument **Nom de la procédure** à **ImprimerFacture\_cliquez sur**.</span><span class="sxs-lookup"><span data-stu-id="66bab-122">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="66bab-123">Pour afficher la procédure événementielle d'un formulaire ou d'un état, celui-ci doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="66bab-123">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="66bab-124">De même, pour ouvrir une procédure dans un module de classe, vous devez spécifier le nom du module, bien que celui-ci ne doit pas être ouvert.</span><span class="sxs-lookup"><span data-stu-id="66bab-124">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="66bab-125">Pour ouvrir une procédure privée, le module qui la contient doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="66bab-125">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="66bab-p106">Cette action revient à cliquer avec le bouton droit sur un module dans le volet de navigation et à cliquer ensuite sur **Mode Création**. Cette action vous permet également de spécifier un nom de procédure et de rechercher les modules standard dans une base de données de procédures.</span><span class="sxs-lookup"><span data-stu-id="66bab-p106">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**. This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>


> [!TIP]
> <P><span data-ttu-id="66bab-p107">[!CONSEIL] Vous pouvez sélectionner un module dans le volet de navigation et le faire glisser vers une ligne d'action de macro. Ceci crée automatiquement une action <STRONG>OuvrirModuleVisualBasic</STRONG> qui ouvre le module dans la section Déclarations.</span><span class="sxs-lookup"><span data-stu-id="66bab-p107">You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an <STRONG>OpenVisualBasicModule</STRONG> action that opens the module to the Declarations section.</span></span></P>



<span data-ttu-id="66bab-130">Pour exécuter l'action **OuvrirModuleVisualBasic** dans un module VBA, utilisez la méthode **OpenModule** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="66bab-130">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

