---
title: Stream, objet (ADO)
TOCTitle: Stream Object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d689e853f1104305a08c1193b098d99935035092
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471409"
---
# <a name="stream-object-ado"></a><span data-ttu-id="0410e-102">Stream, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="0410e-102">Stream Object (ADO)</span></span>


<span data-ttu-id="0410e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0410e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0410e-104">Représente un flux de données binaires ou de texte.</span><span class="sxs-lookup"><span data-stu-id="0410e-104">Represents a stream of binary data or text.</span></span>

## <a name="remarks"></a><span data-ttu-id="0410e-105">Notes</span><span class="sxs-lookup"><span data-stu-id="0410e-105">Remarks</span></span>

<span data-ttu-id="0410e-p101">Dans les hiérarchies en arborescence comme un système de fichiers ou un système de courrier électronique, un objet [Record](record-object-ado.md) peut être associé à un flux de bits binaire par défaut, qui contient le fichier ou le message électronique. Un objet **Stream** peut être utilisé pour manipuler des champs ou des enregistrements contenant ces flux de données. Un objet **Stream** peut être obtenu de différentes façons :</span><span class="sxs-lookup"><span data-stu-id="0410e-p101">In tree-structured hierarchies such as a file system or an e-mail system, a [Record](record-object-ado.md) may have a default binary stream of bits associated with it that contains the contents of the file or the e-mail. A **Stream** object can be used to manipulate fields or records containing these streams of data. A **Stream** object can be obtained in these ways:</span></span>

  - <span data-ttu-id="0410e-p102">À partir d'une URL pointant sur un objet (en général, un fichier) contenant des données binaires ou texte. Cet objet peut être un simple document, un objet **Record** représentant un document structuré ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="0410e-p102">From a URL pointing to an object (typically a file) containing binary or text data. This object can be a simple document, a **Record** object representing a structured document, or a folder.</span></span>

  - <span data-ttu-id="0410e-p103">En ouvrant l'objet **Stream** par défaut associé à un objet **Record**. Vous pouvez obtenir le flux par défaut associé à un objet **Record** lorsque cet objet **Record** est ouvert, ce qui évite un aller-retour qui ne servirait qu'à ouvrir le flux.</span><span class="sxs-lookup"><span data-stu-id="0410e-p103">By opening the default **Stream** object associated with a **Record** object. You can obtain the default stream associated with a **Record** object when the **Record** is opened, to eliminate a round-trip just to open the stream.</span></span>

  - <span data-ttu-id="0410e-p104">Par l'instanciation d'un objet **Stream**. Ces objets **Stream** peuvent être utilisés pour stocker des données afin de répondre aux besoins de votre application. Contrairement au **Stream** associé à une URL ou au **Stream** par défaut d'un **Record**, un **Stream** instancié n'est pas associé à une source sous-jacente par défaut.</span><span class="sxs-lookup"><span data-stu-id="0410e-p104">By instantiating a **Stream** object. These **Stream** objects can be used to store data for the purposes of your application. Unlike a **Stream** associated with a URL, or the default **Stream** of a **Record**, an instantiated **Stream** has no association with an underlying source by default.</span></span>

<span data-ttu-id="0410e-116">Les méthodes et les propriétés d'un objet **Stream** vous permettent d'effectuer diverses tâches :</span><span class="sxs-lookup"><span data-stu-id="0410e-116">With the methods and properties of a **Stream** object, you can do the following:</span></span>

  - <span data-ttu-id="0410e-117">ouvrir un objet **Stream** à partir d'un **Record** ou d'une URL, à l'aide de la méthode [Open](open-method-ado-stream.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-117">Open a **Stream** object from a **Record** or URL with the [Open](open-method-ado-stream.md) method.</span></span>

  - <span data-ttu-id="0410e-118">fermer un **Stream** à l'aide de la méthode [Close](close-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-118">Close a **Stream** with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="0410e-119">entrer des octets ou du texte dans un **Stream** à l'aide des méthodes [Write](write-method-ado.md) et [WriteText](writetext-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-119">Input bytes or text to a **Stream** with the [Write](write-method-ado.md) and [WriteText](writetext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="0410e-120">lire des octets du **Stream** à l'aide des méthodes [Read](read-method-ado.md) et [ReadText](readtext-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-120">Read bytes from the **Stream** with the [Read](read-method-ado.md) and [ReadText](readtext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="0410e-121">écrire des données **Stream** (encore présentes dans le tampon ADO) dans l'objet sous-jacent à l'aide de la méthode [Flush](flush-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-121">Write any **Stream** data still in the ADO buffer to the underlying object with the [Flush](flush-method-ado.md) method.</span></span>

  - <span data-ttu-id="0410e-122">copier le contenu d'un **Stream** dans un autre **Stream** à l'aide de la méthode [CopyTo](copyto-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-122">Copy the contents of a **Stream** to another **Stream** with the [CopyTo](copyto-method-ado.md) method.</span></span>

  - <span data-ttu-id="0410e-123">contrôler la façon dont les lignes sont lues depuis le fichier source avec la méthode [SkipLine](skipline-method-ado.md) et la propriété [LineSeparator](lineseparator-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-123">Control how lines are read from the source file with the [SkipLine](skipline-method-ado.md) method and the [LineSeparator](lineseparator-property-ado.md) property.</span></span>

  - <span data-ttu-id="0410e-124">déterminer la fin de la position du flux à l'aide de la propriété [EOS](eos-property-ado.md) et de la méthode [SetEOS](seteos-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-124">Determine the end of stream position with the [EOS](eos-property-ado.md) property and [SetEOS](seteos-method-ado.md) method.</span></span>

  - <span data-ttu-id="0410e-125">enregistrer et restaurer des données dans des fichiers à l'aide des méthodes [SaveToFile](savetofile-method-ado.md) et [LoadFromFile](loadfromfile-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-125">Save and restore data in files with the [SaveToFile](savetofile-method-ado.md) and [LoadFromFile](loadfromfile-method-ado.md) methods.</span></span>

  - <span data-ttu-id="0410e-126">spécifier le jeu de caractères utilisé pour stocker le **Stream** à l'aide de la propriété [Charset](charset-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-126">Specify the character set used for storing the **Stream** with the [Charset](charset-property-ado.md) property.</span></span>

  - <span data-ttu-id="0410e-127">arrêter une opération **Stream** asynchrone à l'aide de la méthode [Cancel](cancel-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-127">Halt an asynchronous **Stream** operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="0410e-128">déterminer le nombre d'octets d'un **Stream** à l'aide de la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-128">Determine the number of bytes in a **Stream** with the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="0410e-129">contrôler la position actuelle au sein d'un **Stream** à l'aide de la propriété [Position](position-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-129">Control the current position within a **Stream** with the [Position](position-property-ado.md) property.</span></span>

  - <span data-ttu-id="0410e-130">déterminer le type de données dans un **Stream** à l'aide de la propriété [Type](type-property-ado-stream.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-130">Determine the type of data in a **Stream** with the [Type](type-property-ado-stream.md) property.</span></span>

  - <span data-ttu-id="0410e-131">déterminer l'état actuel du **Stream** (fermé, ouvert ou en cours d'exécution) à l'aide de la propriété [State](state-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="0410e-131">Determine the current state of the **Stream** (closed, open, or executing) with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="0410e-132">spécifier le mode d'accès au **Stream** à l'aide de la propriété [Mode](mode-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0410e-132">Specify the access mode for the **Stream** with the [Mode](mode-property-ado.md) property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0410e-p105">[!REMARQUE] Les URL qui utilisent le modèle http appellent automatiquement <A href="microsoft-ole-db-provider-for-internet-publishing.md">Fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, voir <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</span><span class="sxs-lookup"><span data-stu-id="0410e-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


