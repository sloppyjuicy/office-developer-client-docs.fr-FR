---
title: Propriété valeur.champ (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7ed259b1af80f4bd5c51b833462318b6e4696ae
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936188"
---
# <a name="fieldvalue-property-dao"></a><span data-ttu-id="1d838-102">Propriété valeur.champ (DAO)</span><span class="sxs-lookup"><span data-stu-id="1d838-102">Field.Value property (DAO)</span></span>


<span data-ttu-id="1d838-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d838-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d838-p101">Définit ou renvoie la valeur d'un objet. Type de données **Variant** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1d838-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d838-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d838-106">Syntax</span></span>

<span data-ttu-id="1d838-107">*expression* . Valeur</span><span class="sxs-lookup"><span data-stu-id="1d838-107">*expression* .Value</span></span>

<span data-ttu-id="1d838-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="1d838-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d838-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d838-109">Remarks</span></span>

<span data-ttu-id="1d838-110">Le paramètre ou la valeur de retour est un type de données Variant qui est évalué à une valeur appropriée pour le type de données, tel que spécifié par la propriété **Type** d'un objet.</span><span class="sxs-lookup"><span data-stu-id="1d838-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="1d838-111">En général, la propriété **Value** est utilisée pour récupérer et modifier les données dans les objets **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1d838-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="1d838-p102">La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="1d838-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="1d838-114">Si vous essayez de définir ou de renvoyer la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), vous obtenez une erreur interceptable.</span><span class="sxs-lookup"><span data-stu-id="1d838-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <span data-ttu-id="1d838-115">Lorsque vous lisez des valeurs décimales depuis une base de données Microsoft SQL Server, elle sont mises en forme à l'aide d'une notation scientifique via un espace de travail Microsoft Access, mais elles s'affichent sous forme de valeurs décimales normales via un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="1d838-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


