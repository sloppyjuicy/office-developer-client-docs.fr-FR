---
title: Field.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a737f19b33777ea9c3acaf3bc6a9de5144a4db6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874075"
---
# <a name="fieldvalidationrule-property-dao"></a><span data-ttu-id="a904a-102">Field.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a904a-102">Field.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="a904a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a904a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a904a-p101">Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="a904a-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a904a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a904a-106">Syntax</span></span>

<span data-ttu-id="a904a-107">*expression* . ValidationRule (ValideSi)</span><span class="sxs-lookup"><span data-stu-id="a904a-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="a904a-108">*expression* Expression qui renvoie un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="a904a-108">*expression* An expression that returns a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a904a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="a904a-109">Remarks</span></span>

<span data-ttu-id="a904a-p102">Les paramètres ou valeurs de retour sont des chaînes (type String) qui décrivent une comparaison sous la forme d'une clause SQL WHERE sans le mot réservé WHERE. Pour un objet non encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a904a-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="a904a-p103">La propriété **ValidationRule** détermine si un champ contient des données valides. Si les données ne sont pas valides, une erreur d'exécution interceptable se produit. Le message d'erreur renvoyé contient le texte de la propriété **[ValidationText](field-validationtext-property-dao.md)**, si elle est spécifiée, ou le texte de l'expression spécifiée par **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="a904a-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **[ValidationText](field-validationtext-property-dao.md)** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="a904a-115">Pour un objet **[Field](field-object-dao.md)**, l'utilisation de la propriété **ValidationRule** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté.</span><span class="sxs-lookup"><span data-stu-id="a904a-115">For a **[Field](field-object-dao.md)** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a904a-116">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="a904a-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="a904a-117">Utilisation</span><span class="sxs-lookup"><span data-stu-id="a904a-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a904a-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a904a-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="a904a-119">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a904a-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a904a-120"><strong>Objet QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a904a-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a904a-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a904a-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a904a-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a904a-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="a904a-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a904a-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a904a-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a904a-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="a904a-125">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a904a-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a904a-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a904a-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="a904a-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a904a-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a904a-128">La validation est uniquement prise en charge pour les bases de données qui utilisent le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a904a-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="a904a-p104">L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** peut uniquement faire référence à cet objet **Field**. L'expression ne peut pas référencer des fonctions définies par l'utilisateur, des fonctions d'agrégation SQL ou des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque le paramètre de sa propriété **ValidateOnSet** est **True**, il doit être possible d'analyser l'expression (avec le nom du champ comme opérande implicite), laquelle doit correspondre à **True**. Si le paramètre de sa propriété **ValidateOnSet** est **False**, le paramètre de la propriété **ValidationRule** n'est pas pris en compte.</span><span class="sxs-lookup"><span data-stu-id="a904a-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a904a-133">Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strRule = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque votre code tente de valider des données.</span><span class="sxs-lookup"><span data-stu-id="a904a-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="a904a-134">En effet, pendant la concaténation, le nombre est converti en une chaîne qui utilise le caractère décimal par défaut de votre système ; Microsoft Access SQL n'accepte que les caractères décimaux de l'anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="a904a-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>


