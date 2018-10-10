---
title: Field2.Value Property (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ae14ee13c0b94a477550b0f20cec2e1fc31fdd6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470980"
---
# <a name="field2value-property-dao"></a><span data-ttu-id="cf6ed-102">Field2.Value Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="cf6ed-102">Field2.Value Property (DAO)</span></span>


<span data-ttu-id="cf6ed-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf6ed-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cf6ed-p101">Définit ou renvoie la valeur d'un objet. Type de données **Variant** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf6ed-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf6ed-106">Syntax</span></span>

<span data-ttu-id="cf6ed-107">*expression* . Valeur</span><span class="sxs-lookup"><span data-stu-id="cf6ed-107">*expression* .Value</span></span>

<span data-ttu-id="cf6ed-108">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="cf6ed-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf6ed-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf6ed-109">Remarks</span></span>

<span data-ttu-id="cf6ed-110">Le paramètre ou la valeur de retour est un type de données Variant qui est évalué à une valeur appropriée pour le type de données, tel que spécifié par la propriété **Type** d'un objet.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="cf6ed-111">En règle générale, la propriété **Value** permet d'extraire et de modifier les données des objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="cf6ed-p102">La propriété **Value** est la propriété par défaut des objets **Field2**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en leur faisant directement référence plutôt qu'en définissant la propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-p102">The **Value** property is the default property of the **Field2**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="cf6ed-114">Une erreur capturable survient si vous tentez de définir ou de retourner la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field2** de la collection **Fields** d'un objet **TableDef**) entraîne une erreur capturable.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field2** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cf6ed-115">Lorsque vous lisez des valeurs décimales d'une base de données Microsoft SQL Server, elles sont formattées à l'aide d'une notation scientifique dans un espace de travail Microsoft Access, mais apparaissent comme des valeurs décimales normales dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>


