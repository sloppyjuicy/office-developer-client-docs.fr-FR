---
title: TableDef.ValidationRule, propriété (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44329a4cc320e9adcc0612629bcc3fdcd179a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314881"
---
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="61e09-102">TableDef.ValidationRule, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="61e09-102">TableDef.ValidationRule property (DAO)</span></span>

<span data-ttu-id="61e09-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61e09-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61e09-104">Définit ou renvoie une valeur qui valide les données dans un champ au moment de leur modification ou de leur ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="61e09-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61e09-105">Syntax</span></span>

<span data-ttu-id="61e09-106">*.* ValidationRule</span><span class="sxs-lookup"><span data-stu-id="61e09-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="61e09-107">*expression* Variable représentant un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="61e09-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61e09-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="61e09-108">Remarks</span></span>

<span data-ttu-id="61e09-p101">Les paramètres ou valeurs de retour sont des chaînes (type **String**) qui décrivent une comparaison sous la forme d'une clause SQL WHERE sans le mot réservé WHERE. Pour un objet non encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="61e09-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="61e09-p102">La propriété **ValidationRule** détermine si un champ contient des données valides. Si les données ne sont pas valides, une erreur d'exécution interceptable se produit. Le message d'erreur renvoyé contient le texte de la propriété **ValidationText**, si elle est spécifiée, ou le texte de l'expression spécifiée par **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="61e09-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="61e09-114">La validation n'est prise en charge que par les bases de données qui utilisent le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="61e09-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="61e09-p103">L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** ne peut faire référence qu'à cet objet **Field**. L'expression ne peut pas faire référence à des fonctions définies par l'utilisateur, à des fonctions d'agrégation SQL ni à des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque sa propriété **ValidateOnSet** a la valeur **True**, l'expression doit analyser avec succès (avec le nom du champ en tant qu'opérateur implicite) et être évaluée à **True**. Si sa propriété **ValidateOnSet** a la valeur **False**, la valeur de la propriété **ValidationRule** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="61e09-p103">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="61e09-p104">La propriété **ValidationRule** d'un objet **Recordset** ou **TableDef** peut faire référence à plusieurs champs dans cet objet. Les restrictions expliquées plus haut dans cette rubrique pour l'objet **Field** sont applicables.</span><span class="sxs-lookup"><span data-stu-id="61e09-p104">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="61e09-p105">Pour un objet **TableDef** basé sur une table liée, la propriété **ValidationRule** hérite de la valeur de la propriété **ValidationRule** de la table de base sous-jacente. Si celle table ne prend pas en charge la validation, la valeur de cette propriété est une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="61e09-p105">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table. If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>

> [!NOTE]
> <span data-ttu-id="61e09-123">Si vous définissez la propriété sur une chaîne concatentée avec une valeur non-integer, et que les paramètres système spécifient une valeur non américaine. caractère décimal tel qu’une virgule (par exemple, strRule = « PRICE &gt; " &amp; lngPrice et lngPrice = 125,50), une erreur se résulte lorsque votre code tente de valider des données.</span><span class="sxs-lookup"><span data-stu-id="61e09-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="61e09-124">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="61e09-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>
