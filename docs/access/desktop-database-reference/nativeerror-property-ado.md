---
title: NativeError, propriété (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d572e7629deca0c7732bafbdfdb0c600ce34a35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880179"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="be2a4-102">NativeError, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="be2a4-102">NativeError property (ADO)</span></span>


<span data-ttu-id="be2a4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be2a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be2a4-104">Indique le code d'erreur spécifique au fournisseur pour un objet [Error](error-object-ado.md) donné.</span><span class="sxs-lookup"><span data-stu-id="be2a4-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="be2a4-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be2a4-105">Return value</span></span>

<span data-ttu-id="be2a4-106">Renvoie une valeur de type **Long** qui indique le code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="be2a4-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be2a4-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="be2a4-107">Remarks</span></span>

<span data-ttu-id="be2a4-p101">Utilisez la propriété **NativeError** pour récupérer les informations spécifiques à la base de données sur l'objet **Error** concerné. Par exemple, lorsque l'on utilise un fournisseur Microsoft ODBC pour OLE DB avec une base de données Microsoft SQL, les codes d'erreur d'origine provenant de SQL Server transitent par ODBC et par le fournisseur ODBC pour atteindre la propriété **Native Error** ADO.</span><span class="sxs-lookup"><span data-stu-id="be2a4-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

