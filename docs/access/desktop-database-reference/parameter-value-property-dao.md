---
title: Propriété Parameter.Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4e7f3976b934c407a038f321953259fd63a6f60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717439"
---
# <a name="parametervalue-property-dao"></a><span data-ttu-id="f60b7-102">Propriété Parameter.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="f60b7-102">Parameter.Value property (DAO)</span></span>

<span data-ttu-id="f60b7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f60b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f60b7-p101">Définit ou renvoie la valeur d'un objet. Type de données **Variant** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f60b7-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f60b7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f60b7-106">Syntax</span></span>

<span data-ttu-id="f60b7-107">*expression* . Valeur</span><span class="sxs-lookup"><span data-stu-id="f60b7-107">*expression* .Value</span></span>

<span data-ttu-id="f60b7-108">*expression* Variable qui représente un objet **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="f60b7-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f60b7-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="f60b7-109">Remarks</span></span>

<span data-ttu-id="f60b7-110">Le paramètre ou la valeur de retour est un type de données Variant qui est évalué à une valeur appropriée pour le type de données, tel que spécifié par la propriété **Type** d'un objet.</span><span class="sxs-lookup"><span data-stu-id="f60b7-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="f60b7-111">En général, la propriété **Value** est utilisée pour récupérer et modifier les données dans les objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f60b7-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="f60b7-p102">La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="f60b7-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="f60b7-114">Si vous essayez de définir ou de renvoyer la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), vous obtenez une erreur interceptable.</span><span class="sxs-lookup"><span data-stu-id="f60b7-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="f60b7-115">Lorsque vous lisez des valeurs décimales depuis une base de données Microsoft SQL Server, elle sont mises en forme à l'aide d'une notation scientifique via un espace de travail Microsoft Access, mais elles s'affichent sous forme de valeurs décimales normales via un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="f60b7-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


