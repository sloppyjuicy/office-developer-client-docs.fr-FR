---
title: URL absolues et relatives
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a488617dc7ba0d7d1f7e38391f8382fa1e7ed247
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282100"
---
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="8c29f-102">URL absolues et relatives</span><span class="sxs-lookup"><span data-stu-id="8c29f-102">Absolute and relative URLs</span></span>

<span data-ttu-id="8c29f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c29f-103">**Applies to**: Access 2013, Office 2013</span></span>    

<span data-ttu-id="8c29f-104">Une URL spécifie l'emplacement d'une cible sur un ordinateur local ou en réseau, par exemple un fichier, un répertoire, une page HTML, une image, un programme, etc.</span><span class="sxs-lookup"><span data-stu-id="8c29f-104">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on.</span></span> <span data-ttu-id="8c29f-105">Dans cette présentation, une *URL absolue* a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="8c29f-105">In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="8c29f-106">*modèle://serveur/chemin d'accès/ressource*</span><span class="sxs-lookup"><span data-stu-id="8c29f-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="8c29f-107">où :</span><span class="sxs-lookup"><span data-stu-id="8c29f-107">where:</span></span>

|<span data-ttu-id="8c29f-108">Nom</span><span class="sxs-lookup"><span data-stu-id="8c29f-108">Name</span></span> |<span data-ttu-id="8c29f-109">Description</span><span class="sxs-lookup"><span data-stu-id="8c29f-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="8c29f-110">*modèle*</span><span class="sxs-lookup"><span data-stu-id="8c29f-110">*scheme*</span></span>|<span data-ttu-id="8c29f-111">Indique comment accéder à la *ressource*.</span><span class="sxs-lookup"><span data-stu-id="8c29f-111">Specifies how the *resource* is to be accessed.</span></span>|
|<span data-ttu-id="8c29f-112">*Serveur*</span><span class="sxs-lookup"><span data-stu-id="8c29f-112">*server*</span></span>|<span data-ttu-id="8c29f-113">Indique le nom de l'ordinateur où réside la *ressource*.</span><span class="sxs-lookup"><span data-stu-id="8c29f-113">Specifies the name of the computer where the *resource* is located.</span></span>|
|<span data-ttu-id="8c29f-114">*chemin d'accès*</span><span class="sxs-lookup"><span data-stu-id="8c29f-114">*path*</span></span>|<span data-ttu-id="8c29f-115">Indique la séquence de répertoires menant à la cible.</span><span class="sxs-lookup"><span data-stu-id="8c29f-115">Specifies the sequence of directories leading to the target.</span></span> <span data-ttu-id="8c29f-116">Si la *ressource* est omise, la cible est le dernier répertoire figurant dans le *chemin d'accès*.</span><span class="sxs-lookup"><span data-stu-id="8c29f-116">If *resource* is omitted, the target is the last directory in *path*.</span></span>|
|<span data-ttu-id="8c29f-117">*resource*</span><span class="sxs-lookup"><span data-stu-id="8c29f-117">*resource*</span></span>|<span data-ttu-id="8c29f-118">Si elle est incluse, la *ressource* est la cible et indique en général le nom d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="8c29f-118">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="8c29f-119">Il peut s’agit d’un *fichier simple* contenant un seul flux binaire d’octets ou d’un *document* structuré contenant un ou plusieurs stockages et flux binaires d’octets.</span><span class="sxs-lookup"><span data-stu-id="8c29f-119">It may be a *simple file*, containing a single binary stream of bytes, or a *structured document*, containing one or more storages and binary streams of bytes.</span></span>|

<span data-ttu-id="8c29f-120">Une *URL absolue* contient toutes les informations nécessaires pour localiser une ressource.</span><span class="sxs-lookup"><span data-stu-id="8c29f-120">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="8c29f-p104">Une *URL relative* localise une ressource en utilisant une URL absolue comme point de départ. Dans la pratique, l' « URL complète » de la cible est spécifiée par la concaténation des URL absolue et relative. Une URL relative n'est constituée en général que du *chemin d'accès* et, éventuellement, de la *ressource*, mais pas du *modèle* ni du *serveur*.</span><span class="sxs-lookup"><span data-stu-id="8c29f-p104">A *relative URL* locates a resource using an absolute URL as a starting point. In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs. A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="8c29f-124">Enregistrement du schéma d’URL</span><span class="sxs-lookup"><span data-stu-id="8c29f-124">URL scheme registration</span></span>

<span data-ttu-id="8c29f-125">Si un fournisseur prend en charge plusieurs URL, il sera enregistré pour un ou plusieurs modèles d'URL.</span><span class="sxs-lookup"><span data-stu-id="8c29f-125">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="8c29f-126">C'est-à-dire que les URL utilisant ces modèles appelleront automatiquement le fournisseur enregistré.</span><span class="sxs-lookup"><span data-stu-id="8c29f-126">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="8c29f-127">Par exemple, le modèle *http* est enregistré pour le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="8c29f-127">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="8c29f-128">ADO suppose que toutes les URL avec le préfixe « http » représentent des dossiers web ou des fichiers à utiliser avec le fournisseur de publication Internet.</span><span class="sxs-lookup"><span data-stu-id="8c29f-128">ADO assumes all URLs prefixed with "http" represent web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="8c29f-129">Pour plus d'informations sur les modèles enregistrés par votre fournisseur, consultez la documentation de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="8c29f-129">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="8c29f-130">Définition d’un contexte avec une URL</span><span class="sxs-lookup"><span data-stu-id="8c29f-130">Defining context with a URL</span></span>

<span data-ttu-id="8c29f-p106">Une des fonctions d'une connexion ouverte, représentée par un objet [Connection](connection-object-ado.md), est de limiter les opérations ultérieures sur la source de données représentée par cette connexion. En d'autres termes, la connexion définit le contexte des opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c29f-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="8c29f-p107">Avec ADO 2.5, une URL absolue peut également définir un contexte. Par exemple, lorsqu'un objet [Record](record-object-ado.md) est ouvert avec une URL absolue, un objet **Connection** est implicitement créé pour représenter la ressource spécifiée par l'URL.</span><span class="sxs-lookup"><span data-stu-id="8c29f-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="8c29f-135">Une URL absolue qui définit un contexte peut être spécifiée dans le nouveau paramètre *ActiveConnection* de la méthode [Open](open-method-ado-record.md) de l'objet **Record**.</span><span class="sxs-lookup"><span data-stu-id="8c29f-135">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="8c29f-136">Une URL absolue peut également être spécifiée en tant que valeur du nouveau mot clé dans le paramètre `URL=` *ConnectionString* de la méthode [Open](open-method-ado-connection.md) de l’objet **Connection** et du paramètre *ActiveConnection* de la méthode [Open](open-method-ado-recordset.md) de l’objet [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8c29f-136">An absolute URL may also be specified as the value of the new `URL=` keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="8c29f-137">Le contexte peut également être défini avec un objet **Record** ou **Recordset** ouvert qui représente un répertoire, car ces objets disposent déjà d'un objet **Connection** implicitement ou explicitement déclaré qui spécifie le contexte.</span><span class="sxs-lookup"><span data-stu-id="8c29f-137">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="8c29f-138">Opérations limitées</span><span class="sxs-lookup"><span data-stu-id="8c29f-138">Scoped operations</span></span>

<span data-ttu-id="8c29f-139">Le contexte définit simultanément une *étendue,* c’est-à-dire le répertoire et ses sous-répertoires qui peuvent participer aux opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c29f-139">The context simultaneously defines a *scope*—that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="8c29f-140">L'objet **Record** comporte plusieurs méthodes de portée définie, notamment [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) et [DeleteRecord](deleterecord-method-ado.md) qui s'appliquent à un répertoire et à ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="8c29f-140">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](deleterecord-method-ado.md), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="8c29f-141">URL relatives en tant que texte de commande</span><span class="sxs-lookup"><span data-stu-id="8c29f-141">Relative URLs as command text</span></span>

<span data-ttu-id="8c29f-142">Il est possible de spécifier une commande à exécuter sur la source de données dans le paramètre *CommandText* de la méthode **Execute** de l'objet **Connection** et le paramètre *Source* de la méthode **Open** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8c29f-142">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="8c29f-p110">Il est également possible de spécifier une URL relative dans le paramètre *CommandText* ou *Source*. L'URL relative ne spécifie pas une commande (comme une commande SQL) ; elle est simplement spécifiée dans ces paramètres. En outre, le contexte de la connexion active doit être une URL absolue et le paramètre *Option* doit avoir la valeur **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="8c29f-p110">A relative URL may be specified in the *CommandText* or *Source* parameter. The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters. In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="8c29f-146">Par exemple, un objet **Recordset** peut être ouvert sur le fichier Readme25.txt du répertoire Winnt/system32 comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c29f-146">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="8c29f-147">L’URL absolue dans la chaîne de connexion spécifie le serveur (YourServer) et le chemin d’accès (Winnt).</span><span class="sxs-lookup"><span data-stu-id="8c29f-147">The absolute URL in the connection string specifies the server (YourServer) and the path (Winnt).</span></span> <span data-ttu-id="8c29f-148">Cette URL définit également le contexte.</span><span class="sxs-lookup"><span data-stu-id="8c29f-148">This URL also defines the context.</span></span>

<span data-ttu-id="8c29f-149">L’URL relative dans le texte de commande utilise l’URL absolue comme point de départ et spécifie le reste du chemin d’accès (system32) et le fichier à ouvrir (Readme25.txt).</span><span class="sxs-lookup"><span data-stu-id="8c29f-149">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32) and the file to open (Readme25.txt).</span></span>

<span data-ttu-id="8c29f-150">Le champ Options indique que le type de commande est une URL relative.</span><span class="sxs-lookup"><span data-stu-id="8c29f-150">The options field indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="8c29f-151">Autre exemple : le code suivant ouvre un **recordset** sur le contenu du répertoire :</span><span class="sxs-lookup"><span data-stu-id="8c29f-151">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="8c29f-152">Schémas d’URL fournis par le fournisseur OLE DB</span><span class="sxs-lookup"><span data-stu-id="8c29f-152">OLE DB provider-supplied URL schemes</span></span>

<span data-ttu-id="8c29f-p112">Le début d'une URL complète est le *modèle* utilisé pour accéder à la ressource identifiée par le reste de l'URL. Par exemple, HTTP (HyperText Transfer Protocol) et FTP (File Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="8c29f-p112">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL. Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="8c29f-155">ADO supports OLE DB providers that recognize their own URL schemes.</span><span class="sxs-lookup"><span data-stu-id="8c29f-155">ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="8c29f-156">Par exemple, le fournisseur [Microsoft OLE DB](microsoft-ole-db-provider-for-internet-publishing.md)pour la publication Internet, qui accède aux fichiers Windows 2000 « publiés », reconnaît le schéma HTTP existant.</span><span class="sxs-lookup"><span data-stu-id="8c29f-156">For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

