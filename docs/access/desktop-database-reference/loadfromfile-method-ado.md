---
title: LoadFromFile, méthode (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96bc0f55f6524a2aaa04bbe1f9b591ff2eb85bb8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925722"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="65390-102">LoadFromFile, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="65390-102">LoadFromFile method (ADO)</span></span>


<span data-ttu-id="65390-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65390-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="65390-104">Charge le contenu d'un fichier existant dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="65390-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="65390-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65390-105">Syntax</span></span>

<span data-ttu-id="65390-106">*Flux de données*. LoadFromFile, *nom de fichier*</span><span class="sxs-lookup"><span data-stu-id="65390-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameter"></a><span data-ttu-id="65390-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="65390-107">Parameter</span></span>

  - <span data-ttu-id="65390-108">*FileName*</span><span class="sxs-lookup"><span data-stu-id="65390-108">*FileName*</span></span>

  - <span data-ttu-id="65390-109">Valeur de type **String** qui contient le nom d'un fichier à charger dans l'objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="65390-109">A **String** value that contains the name of a file to be loaded into the **Stream**.</span></span> <span data-ttu-id="65390-110">*Nom de fichier* peut contenir n’importe quel chemin d’accès valide et un nom au format UNC.</span><span class="sxs-lookup"><span data-stu-id="65390-110">*FileName* can contain any valid path and name in UNC format.</span></span> <span data-ttu-id="65390-111">Si le fichier spécifié n'existe pas, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="65390-111">If the specified file does not exist, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="65390-112">Notes</span><span class="sxs-lookup"><span data-stu-id="65390-112">Remarks</span></span>

<span data-ttu-id="65390-p102">Cette méthode peut être utilisée pour charger le contenu d'un fichier local dans un objet **Stream**. Cela permet de télécharger le contenu d'un fichier local sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="65390-p102">This method may be used to load the contents of a local file into a **Stream** object. This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="65390-p103">L'objet **Stream** doit être déjà ouvert avant d'appeler la méthode **LoadFromFile**. Cette méthode ne modifie pas la liaison de l'objet **Stream**; il sera toujours lié à l'objet spécifié par l'URL ou l'objet **Record** avec lequel l'objet **Stream** a été initialement ouvert.</span><span class="sxs-lookup"><span data-stu-id="65390-p103">The **Stream** object must be already open before calling **LoadFromFile**. This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="65390-p104">La méthode **LoadFromFile** remplace le contenu actuel de l'objet **Stream** par les données lues à partir du fichier. Tous les octets présents dans l'objet **Stream** sont remplacés par le contenu du fichier. Tous les octets qui existaient déjà ou restent encore après la création de la propriété [EOS](eos-property-ado.md) par **LoadFromFile** sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="65390-p104">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file. Any existing bytes in the **Stream** are overwritten by the contents of the file. Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="65390-120">Après un appel de la méthode **LoadFromFile**, la position actuelle est définie au début de l’objet **Stream** ([Position](position-property-ado.md) est 0).</span><span class="sxs-lookup"><span data-stu-id="65390-120">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="65390-121">Dans la mesure où 2 octets peuvent être ajoutés au début du flux pour des raisons de codage, il se peut que la taille du flux ne corresponde pas exactement à celle du fichier à partir duquel il a été chargé.</span><span class="sxs-lookup"><span data-stu-id="65390-121">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

