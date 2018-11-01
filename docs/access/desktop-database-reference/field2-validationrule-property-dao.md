---
title: Field2.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 006c9ce982aa98f28187d04fced12992d61548d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880053"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="c810a-102">Field2.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c810a-102">Field2.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="c810a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c810a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c810a-p101">Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="c810a-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c810a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c810a-106">Syntax</span></span>

<span data-ttu-id="c810a-107">*expression* . ValidationRule (ValideSi)</span><span class="sxs-lookup"><span data-stu-id="c810a-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="c810a-108">*expression* Expression qui renvoie un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="c810a-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c810a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c810a-109">Remarks</span></span>

<span data-ttu-id="c810a-p102">Les paramètres ou les valeurs de retour sont une chaîne qui décrit une comparaison sous la forme d'une clause SQL WHERE sans le mot réservé WHERE. Pour un objet pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c810a-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="c810a-p103">La propriété **ValidationRule** détermine si un champ contient ou non des données valides. Si les données ne sont pas valides, une erreur d'exécution capturable survient. Le message d'erreur renvoyé est le texte de la propriété **ValidationText**, s'il est spécifié, ou le texte de l'expression spécifié par **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="c810a-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="c810a-115">Pour un objet **Field2**, l'utilisation de la propriété **ValidationRule** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté.</span><span class="sxs-lookup"><span data-stu-id="c810a-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c810a-116">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="c810a-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="c810a-117">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c810a-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c810a-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="c810a-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="c810a-119">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="c810a-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c810a-120"><strong>Objet QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="c810a-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c810a-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c810a-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c810a-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="c810a-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="c810a-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c810a-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c810a-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="c810a-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="c810a-125">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="c810a-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c810a-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="c810a-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c810a-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c810a-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c810a-128">La validation n'est prise en charge que par les bases de données qui utilisent le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c810a-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="c810a-p104">L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field2** peut se référer uniquement à ce champ **Field2**. Elle ne peut pas se référer aux fonctions personnalisées, aux fonctions agrégées SQL ou aux requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field2** lorsque son paramètre de propriété **ValidateOnSet** est **True**, l'expression doit analyser avec succès (avec le nom du champ comme opérande implicite) et évaluer à **True**. Si son paramètre de propriété **ValidateOnSet** est **False**, le paramètre de propriété **ValidationRule** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c810a-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c810a-133">Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strRule = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque votre code tente de valider des données.</span><span class="sxs-lookup"><span data-stu-id="c810a-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="c810a-134">En effet, pendant la concaténation, le nombre est converti en une chaîne qui utilise le caractère décimal par défaut de votre système ; Microsoft Access SQL n'accepte que les caractères décimaux de l'anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="c810a-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>


