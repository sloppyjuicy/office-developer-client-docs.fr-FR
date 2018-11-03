---
title: Find, méthode - ActiveX Data Objects (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ff66a39de070759e0ad31b441e4be5735d87516
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936609"
---
# <a name="find-method-ado"></a><span data-ttu-id="6b0f1-102">Find, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="6b0f1-102">Find method (ADO)</span></span>


<span data-ttu-id="6b0f1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b0f1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6b0f1-p101">Recherche un objet [Recordset](recordset-object-ado.md) pour la ligne qui répond aux critères spécifiés. Il est éventuellement possible de spécifier des paramètres facultatifs, tels que la direction de la recherche, la ligne de début et un décalage par rapport à la ligne de début. Si les critères sont satisfaits, la position de ligne actuelle est définie sur l'enregistrement identifié ; sinon la position est définie à la fin (ou au début) de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p101">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b0f1-107">Syntax</span></span>

<span data-ttu-id="6b0f1-108">Rechercher (*critères*, *SkipRows*, *SearchDirection*, *Démarrer*)</span><span class="sxs-lookup"><span data-stu-id="6b0f1-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6b0f1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b0f1-109">Parameters</span></span>

  - <span data-ttu-id="6b0f1-110">*Critères*</span><span class="sxs-lookup"><span data-stu-id="6b0f1-110">*Criteria*</span></span>

  - <span data-ttu-id="6b0f1-111">Une valeur de type **String** qui contient une instruction spécifiant le nom de colonne, l'opérateur de comparaison et la valeur à utiliser dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-111">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>

  - <span data-ttu-id="6b0f1-112">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="6b0f1-112">*SkipRows*</span></span>

  - <span data-ttu-id="6b0f1-p102">Facultatif *.* Valeur de type **Long**, dont la valeur par défaut est zéro et qui spécifie le décalage de lignes par rapport à la ligne active ou un signet *Start* à partir duquel commencer la recherche. Par défaut, la recherche commence à partir de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p102">Optional *.* A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search. By default, the search will start on the current row.</span></span>

  - <span data-ttu-id="6b0f1-116">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="6b0f1-116">*SearchDirection*</span></span>

  - <span data-ttu-id="6b0f1-p103">Facultatif *.* Valeur [SearchDirectionEnum](searchdirectionenum.md) qui spécifie si la recherche doit commencer à partir de la ligne active ou de la ligne disponible suivante selon la direction de la recherche. Une recherche qui ne donne aucun résultat s’arrête à la fin de l’objet **Recordset** si la valeur est **adSearchForward**. En revanche, elle s’arrête au début de l’objet **Recordset** si la valeur est **adSearchBackward**.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p103">Optional *.* A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search. An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**. An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>

  - <span data-ttu-id="6b0f1-121">*Début*</span><span class="sxs-lookup"><span data-stu-id="6b0f1-121">*Start*</span></span>

  - <span data-ttu-id="6b0f1-p104">Facultatif. Signet de type **Variant** qui indique la position de début de la recherche.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p104">Optional. A **Variant** bookmark that functions as the starting position for the search.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b0f1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6b0f1-124">Remarks</span></span>

<span data-ttu-id="6b0f1-p105">Un seul nom de colonne peut être spécifié dans *Critères*. Cette méthode ne prend pas en charge les recherches dans plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p105">Only a single-column name may be specified in *criteria*. This method does not support multi-column searches.</span></span>

<span data-ttu-id="6b0f1-127">L’opérateur de comparaison dans *critères* peut être «**\>**« (supérieur à), »**\<**« (inférieur à), « = » (égal à), »\>= » (supérieur ou égal à), «\<= » (inférieur ou égal à), «\<\>» (différent de), ou « like » (correspondance).</span><span class="sxs-lookup"><span data-stu-id="6b0f1-127">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="6b0f1-128">La valeur de *critères* peut être une chaîne, un nombre à virgule flottante ou une date.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-128">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="6b0f1-129">Valeurs de chaîne sont délimitées par des guillemets simples ou «\#» (signe dièse) marque (par exemple, « état = 'WA' » ou « état = \#WA\#»).</span><span class="sxs-lookup"><span data-stu-id="6b0f1-129">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="6b0f1-130">Valeurs de date sont délimitées par des «\#» (signe dièse) marque (par exemple, « démarrer\_date \> \#7/22/97\#») et peuvent contenir des heures, minutes et secondes pour indiquer l’horodatage mais ne doivent pas contenir de millisecondes ou erreurs seront produit .</span><span class="sxs-lookup"><span data-stu-id="6b0f1-130">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="6b0f1-p107">Si l'opérateur de comparaison est « like », la valeur de chaîne peut contenir un astérisque (\*) pour rechercher une ou plusieurs occurrences d'un caractère ou sous-chaîne. Par exemple, « state like 'M\*' »" correspond aux états du Maine et du Massachusetts. Vous pouvez également utiliser des astérisques de début ou de fin pour rechercher une sous-chaîne contenue dans les valeurs. Par exemple, « state like '\*as\*' »" correspond aux états de l'Alaska, de l'Arkansas et du Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p107">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="6b0f1-p108">Les astérisques peuvent uniquement être utilisés à la fin d'une chaîne de critères ou au début et à la fin de celle-ci, comme illustré ci-dessus. Vous ne pouvez pas l'employer comme caractère générique de début ('\*str') ou incorporé ('s\*r'). Cela provoque une erreur.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p108">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r'). This will cause an error.</span></span>


> [!NOTE]
> <span data-ttu-id="6b0f1-p109">[!REMARQUE] Une erreur se produit si la position de ligne actuelle n'est pas définie avant d'appeler **Find**. Toute méthode qui définit la position de ligne, par exemple [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), doit être appelée avant la méthode **Find**.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p109">An error will occur if a current row position is not set before calling **Find**. Any method that sets row position, such as [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), should be called before calling **Find**.</span></span>

> [!NOTE]
> <span data-ttu-id="6b0f1-p110">[!REMARQUE] Si vous appelez la méthode **Find** sur un jeu d'enregistrements et que la position actuelle dans le jeu d'enregistrements correspond au dernier enregistrement ou à la fin du fichier (EOF), votre recherche ne donne aucun résultat. Vous devez appeler la méthode **MoveFirst** pour définir la position/le curseur actuel au début du jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="6b0f1-p110">If you call the **Find** method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything. You need to call the **MoveFirst** method to set the current position/cursor to the beginning of the recordset.</span></span>


