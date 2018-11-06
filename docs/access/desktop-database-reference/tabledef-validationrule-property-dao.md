---
title: Propriété TableDef.ValidationRule (DAO)
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
ms.openlocfilehash: 47dbb798a0b293f1651308de9aa2064e1c421a07
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996859"
---
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="4a68f-102">Propriété TableDef.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a68f-102">TableDef.ValidationRule property (DAO)</span></span>

<span data-ttu-id="4a68f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a68f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a68f-104">Définit ou renvoie une valeur qui valide les données d'un champ pendant sa modification ou son ajout à une table (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="4a68f-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a68f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a68f-105">Syntax</span></span>

<span data-ttu-id="4a68f-106">*expression* . ValidationRule (ValideSi)</span><span class="sxs-lookup"><span data-stu-id="4a68f-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="4a68f-107">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="4a68f-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a68f-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a68f-108">Remarks</span></span>

<span data-ttu-id="4a68f-p101">Les paramètres ou valeurs de retour sont de type **String**. Cette chaîne décrit une comparaison sous une forme similaire à une clause SQL WHERE sans le mot réservé WHERE. Pour un objet qui n'a pas encore été ajouté à la collection **Fields**, cette propriété est en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="4a68f-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="4a68f-p102">La propriété **ValidationRule** détermine si un champ contient des données valides. Si les données ne sont pas valides, une erreur d'exécution interceptable se produit. Le message d'erreur renvoyé contient le texte de la propriété **ValidationText**, si elle est spécifiée, ou le texte de l'expression spécifiée par **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="4a68f-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="4a68f-114">La validation n'est prise en charge que par les bases de données qui utilisent le moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4a68f-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="4a68f-p103">L'expression de chaîne spécifiée par la propriété **ValidationRule** d'un objet **Field** peut uniquement faire référence à cet objet **Field**. L'expression ne peut pas référencer des fonctions définies par l'utilisateur, des fonctions d'agrégation SQL ou des requêtes. Pour définir la propriété **ValidationRule** d'un objet **Field** lorsque le paramètre de sa propriété **ValidateOnSet** est **True**, il doit être possible d'analyser l'expression (avec le nom du champ comme opérande implicite), laquelle doit correspondre à **True**. Si le paramètre de sa propriété **ValidateOnSet** est **False**, le paramètre de la propriété **ValidationRule** n'est pas pris en compte.</span><span class="sxs-lookup"><span data-stu-id="4a68f-p103">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="4a68f-p104">La propriété **ValidationRule** d'un objet **Recordset** ou **TableDef** peut faire référence à plusieurs champs dans cet objet. Les restrictions expliquées plus haut dans cette rubrique pour l'objet **Field** sont applicables.</span><span class="sxs-lookup"><span data-stu-id="4a68f-p104">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="4a68f-p105">Pour un objet **TableDef** basé sur une table liée, la propriété **ValidationRule** hérite de la valeur de la propriété **ValidationRule** de la table de base sous-jacente. Si celle table ne prend pas en charge la validation, la valeur de cette propriété est une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="4a68f-p105">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table. If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>

> [!NOTE]
> <span data-ttu-id="4a68f-123">Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strRule = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque votre code tente de valider des données.</span><span class="sxs-lookup"><span data-stu-id="4a68f-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="4a68f-124">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="4a68f-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>