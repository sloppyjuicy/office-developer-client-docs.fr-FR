---
title: Recordset2. Filter, propriété (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307328"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="36c1c-102">Recordset2. Filter, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="36c1c-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="36c1c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="36c1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36c1c-104">Définit ou renvoie une valeur qui détermine les enregistrements inclus dans l'objet **Recordset** ouvert ultérieurement (espace de travail Microsoft Access uniquement.</span><span class="sxs-lookup"><span data-stu-id="36c1c-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="36c1c-105">Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="36c1c-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c1c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36c1c-106">Syntax</span></span>

<span data-ttu-id="36c1c-107">*expression* . Éliminer</span><span class="sxs-lookup"><span data-stu-id="36c1c-107">*expression* .Filter</span></span>

<span data-ttu-id="36c1c-108">*expression* Expression qui renvoie un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="36c1c-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c1c-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="36c1c-109">Remarks</span></span>

<span data-ttu-id="36c1c-110">Le paramètre ou la valeur de retour est un type de données String qui contient une clause WHERE d'une instruction SQL sans le mot réservé WHERE.</span><span class="sxs-lookup"><span data-stu-id="36c1c-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="36c1c-111">Utilisez la propriété **Filter** pour appliquer un filtre à un objet **Recordset** de type feuille de réponse dynamique, instantané ou avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="36c1c-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="36c1c-112">La propriété **Filter** permet de limiter le nombre d’enregistrements renvoyés à partir d’un objet existant lorsqu’un nouvel objet **Recordset** est ouvert sur la base d’un objet **Recordset** existant.</span><span class="sxs-lookup"><span data-stu-id="36c1c-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="36c1c-113">Utiliser le format de date américain (mois-jour-année) lorsque vous filtrez des champs contenant des dates, même si vous n'utilisez pas la version américaine du moteur de base de données Microsoft Access (auquel cas vous devez assembler n'importe quelle date en concaténant des chaînes, par exemple, strMonth & "-" _ aMP_ strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="36c1c-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="36c1c-114">Sinon, il est possible que le filtrage des données ne donne pas les résultats escomptés.</span><span class="sxs-lookup"><span data-stu-id="36c1c-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="36c1c-115">Dans la plupart des cas, il est plus rapide d'ouvrir un nouvel objet **Recordset** à l'aide d'une instruction SQL qui comprend une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="36c1c-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="36c1c-116">Si vous affectez à la propriété une chaîne concaténée avec une valeur non entière et que les paramètres système spécifient un caractère non-U. S. Decimal tel qu'une virgule (par exemple, strFilter = " \> Price" & lngPrice et lngPrice = 125, 50), une erreur se produit lorsque vous essayez de ouvre le **jeu d'enregistrements**suivant.</span><span class="sxs-lookup"><span data-stu-id="36c1c-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="36c1c-117">En effet, pendant la concaténation, le nombre est converti en une chaîne qui utilise le caractère décimal par défaut de votre système ; Microsoft Access SQL n'accepte que les caractères décimaux de l'anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="36c1c-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

