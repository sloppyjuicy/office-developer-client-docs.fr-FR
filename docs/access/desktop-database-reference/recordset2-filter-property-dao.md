---
title: Propriété Recordset2.Filter (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720351"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="3d2bc-102">Propriété Recordset2.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="3d2bc-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="3d2bc-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d2bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d2bc-p101">Définit ou renvoie une valeur qui détermine les enregistrements inclus dans un objet **Recordset** ouvert par la suite (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2bc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d2bc-106">Syntax</span></span>

<span data-ttu-id="3d2bc-107">*expression* . Filtre</span><span class="sxs-lookup"><span data-stu-id="3d2bc-107">*expression* .Filter</span></span>

<span data-ttu-id="3d2bc-108">*expression* Expression qui renvoie un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3d2bc-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2bc-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d2bc-109">Remarks</span></span>

<span data-ttu-id="3d2bc-110">Le paramètre ou la valeur de retour est un type de données String qui contient une clause WHERE d'une instruction SQL sans le mot réservé WHERE.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="3d2bc-111">Utilisez la propriété **Filter** pour appliquer un filtre à un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="3d2bc-112">La propriété **Filter** permet de limiter le nombre d'enregistrements renvoyés à partir d'un objet existant lorsqu'un nouvel objet **Recordset** est ouvert sur la base d'un objet **Recordset** existant.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="3d2bc-113">Utilisez le format de date américain (mois-jour-année) lorsque vous filtrez des champs contenant des dates, même si vous n’utilisez pas la version de moteur de base de données Microsoft Access (dans ce cas, vous devez assembler les dates en concaténant des chaînes, par exemple, strMonth & «- » _ aMP_ strDay & «- » & strYear).</span><span class="sxs-lookup"><span data-stu-id="3d2bc-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="3d2bc-114">Sinon, il est possible que le filtrage des données ne donne pas les résultats escomptés.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="3d2bc-115">Dans la plupart des cas, il est plus rapide d'ouvrir un nouvel objet **Recordset** à l'aide d'une instruction SQL qui inclut une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="3d2bc-116">Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strFilter = « prix \> » & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez de Ouvrez le prochain **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="3d2bc-117">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="3d2bc-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

