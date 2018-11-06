---
title: Propriété Property.Value (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4eb1a961a91bf32a69154a1f0e7b734dd00f24b6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998895"
---
# <a name="propertyvalue-property-dao"></a><span data-ttu-id="b5a63-102">Propriété Property.Value (DAO)</span><span class="sxs-lookup"><span data-stu-id="b5a63-102">Property.Value property (DAO)</span></span>

<span data-ttu-id="b5a63-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5a63-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5a63-p101">Définit ou renvoie la valeur d'un objet. Type de données **Variant** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b5a63-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a63-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5a63-106">Syntax</span></span>

<span data-ttu-id="b5a63-107">*expression* . Valeur</span><span class="sxs-lookup"><span data-stu-id="b5a63-107">*expression* .Value</span></span>

<span data-ttu-id="b5a63-108">*expression* Variable qui représente un objet **Property** .</span><span class="sxs-lookup"><span data-stu-id="b5a63-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a63-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="b5a63-109">Remarks</span></span>

<span data-ttu-id="b5a63-110">Le paramètre ou la valeur de retour est un type de données Variant qui est évalué à une valeur appropriée pour le type de données, tel que spécifié par la propriété **Type** d'un objet.</span><span class="sxs-lookup"><span data-stu-id="b5a63-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="b5a63-111">En général, la propriété **Value** est utilisée pour récupérer et modifier les données dans les objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b5a63-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="b5a63-p102">La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="b5a63-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="b5a63-114">Si vous essayez de définir ou de renvoyer la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), vous obtenez une erreur interceptable.</span><span class="sxs-lookup"><span data-stu-id="b5a63-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="b5a63-115">Lorsque vous lisez des valeurs décimales depuis une base de données Microsoft SQL Server, elle sont mises en forme à l'aide d'une notation scientifique via un espace de travail Microsoft Access, mais elles s'affichent sous forme de valeurs décimales normales via un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="b5a63-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


