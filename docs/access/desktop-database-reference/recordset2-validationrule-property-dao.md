---
title: Recordset2.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0c6df32c37f73dadf1df43201090d44d81a6a01
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890945"
---
# <a name="recordset2validationrule-property-dao"></a><span data-ttu-id="8f646-102">Recordset2.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="8f646-102">Recordset2.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="8f646-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f646-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f646-104">Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="8f646-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f646-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f646-105">Syntax</span></span>

<span data-ttu-id="8f646-106">*expression* . ValidationRule (ValideSi)</span><span class="sxs-lookup"><span data-stu-id="8f646-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="8f646-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="8f646-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f646-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f646-108">Remarks</span></span>

<span data-ttu-id="8f646-p101">Les paramètres ou valeurs de retour sont de type **String**. Cette chaîne décrit une comparaison sous une forme similaire à une clause SQL WHERE sans le mot réservé WHERE. Pour un objet qui n'a pas encore été ajouté à la collection **Fields**, cette propriété est en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="8f646-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="8f646-p102">La propriété **ValidationRule** détermine si un champ contient des données valides. Si ce n'est pas le cas, une erreur d'exécution piégeable se produit. Le message d'erreur renvoyé représente le texte de la propriété **ValidationText**, si cette propriété a été définie, ou le texte de l'expression spécifié par la propriété **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="8f646-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="8f646-114">Pour un objet **Recordset** , l’utilisation de la propriété **ValidationRule** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8f646-114">For a **Recordset** object, use of the **ValidationRule** property is read-only.</span></span> <span data-ttu-id="8f646-115">Pour un objet **TableDef** , la propriété **ValidationRule** dépend de l’état de l’objet **TableDef** , comme le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8f646-115">For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f646-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="8f646-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="8f646-117">Utilisation</span><span class="sxs-lookup"><span data-stu-id="8f646-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f646-118">Table de base</span><span class="sxs-lookup"><span data-stu-id="8f646-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="8f646-119">En lecture-écriture</span><span class="sxs-lookup"><span data-stu-id="8f646-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f646-120">Table liée</span><span class="sxs-lookup"><span data-stu-id="8f646-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="8f646-121">En lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f646-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f646-122">La validation est uniquement prise en charge pour les bases de données qui utilisent le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8f646-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="8f646-p104">L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** peut uniquement faire référence à cet objet **Field**. L'expression ne peut pas référencer des fonctions définies par l'utilisateur, des fonctions d'agrégation SQL ou des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque le paramètre de sa propriété **ValidateOnSet** est **True**, il doit être possible d'analyser l'expression (avec le nom du champ comme opérande implicite), laquelle doit correspondre à **True**. Si le paramètre de sa propriété **ValidateOnSet** est **False**, le paramètre de la propriété **ValidationRule** n'est pas pris en compte.</span><span class="sxs-lookup"><span data-stu-id="8f646-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="8f646-p105">La propriété **ValidationRule** d'un objet **Recordset** ou **TableDef** peut référencer plusieurs champs de cet objet. Les restrictions mentionnées ci-dessus relatives à l'objet **Field** sont d'application.</span><span class="sxs-lookup"><span data-stu-id="8f646-p105">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="8f646-129">Pour un objet **Recordset** de type table, la propriété **ValidationRule** hérite du paramètre de la propriété **ValidationRule** de l'objet **TableDef** utilisé pour créer l'objet **Recordset** de type table.</span><span class="sxs-lookup"><span data-stu-id="8f646-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8f646-130">Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strRule = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque votre code tente de valider des données.</span><span class="sxs-lookup"><span data-stu-id="8f646-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="8f646-131">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="8f646-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>


