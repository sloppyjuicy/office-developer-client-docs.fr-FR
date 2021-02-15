---
title: LoadFromFile, méthode (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9316bc4302a559fa44082a0576595707157e9d64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289884"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="45e0e-102">LoadFromFile, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="45e0e-102">LoadFromFile method (ADO)</span></span>

<span data-ttu-id="45e0e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45e0e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45e0e-104">Charge le contenu d’un fichier existant dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="45e0e-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45e0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45e0e-105">Syntax</span></span>

<span data-ttu-id="45e0e-106">*Stream*. LoadFromFile *FileName*</span><span class="sxs-lookup"><span data-stu-id="45e0e-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="45e0e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45e0e-107">Parameters</span></span>

|<span data-ttu-id="45e0e-108">Nom</span><span class="sxs-lookup"><span data-stu-id="45e0e-108">Name</span></span> |<span data-ttu-id="45e0e-109">Description</span><span class="sxs-lookup"><span data-stu-id="45e0e-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="45e0e-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="45e0e-110">*FileName*</span></span> |<span data-ttu-id="45e0e-p101">Valeur de type **String** qui contient le nom d'un fichier à charger dans l'objet **Stream**.  *NomFichier* peut contenir n'importe quel chemin d'accès et nom valide au format UNC. Si le fichier spécifié n'existe pas, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="45e0e-p101">A **String** value that contains the name of a file to be loaded into the **Stream**. *FileName* can contain any valid path and name in UNC format. If the specified file does not exist, a run-time error occurs.</span></span>|

## <a name="remarks"></a><span data-ttu-id="45e0e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="45e0e-114">Remarks</span></span>

<span data-ttu-id="45e0e-p102">Cette méthode peut être utilisée pour charger le contenu d'un fichier local dans un objet **Stream**. Cela permet de télécharger le contenu d'un fichier local sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="45e0e-p102">This method may be used to load the contents of a local file into a **Stream** object. This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="45e0e-p103">L'objet **Stream** doit être déjà ouvert avant d'appeler la méthode **LoadFromFile**. Cette méthode ne modifie pas la liaison de l'objet **Stream**; il sera toujours lié à l'objet spécifié par l'URL ou l'objet **Record** avec lequel l'objet **Stream** a été initialement ouvert.</span><span class="sxs-lookup"><span data-stu-id="45e0e-p103">The **Stream** object must be already open before calling **LoadFromFile**. This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="45e0e-p104">La méthode **LoadFromFile** remplace le contenu actuel de l'objet **Stream** par les données lues à partir du fichier. Tous les octets présents dans l'objet **Stream** sont remplacés par le contenu du fichier. Tous les octets qui existaient déjà ou restent encore après la création de la propriété [EOS](eos-property-ado.md) par **LoadFromFile** sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="45e0e-p104">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file. Any existing bytes in the **Stream** are overwritten by the contents of the file. Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="45e0e-122">Après un appel de la méthode **LoadFromFile**, la position actuelle est définie au début de l’objet **Stream** ([Position](position-property-ado.md) est 0).</span><span class="sxs-lookup"><span data-stu-id="45e0e-122">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="45e0e-123">Dans la mesure où 2 octets peuvent être ajoutés au début du flux pour des raisons de codage, il se peut que la taille du flux ne corresponde pas exactement à celle du fichier à partir duquel il a été chargé.</span><span class="sxs-lookup"><span data-stu-id="45e0e-123">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

