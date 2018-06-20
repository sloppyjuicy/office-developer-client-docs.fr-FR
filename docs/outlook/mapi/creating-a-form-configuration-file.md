---
title: Création d’un fichier de Configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783106"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="77d78-103">Création d’un fichier de Configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="77d78-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="77d78-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77d78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77d78-105">Un fichier de configuration de formulaire fournit des informations sur un formulaire à la fois dans le Gestionnaire de formulaire utilisée et pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="77d78-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="77d78-106">Un fichier de configuration de formulaire contient une spécification d’étendue pour un formulaire, y compris les propriétés publiées par le formulaire pour une utilisation par les clients, les verbes implémentées par le formulaire et les plateformes prises en charge par le formulaire de messagerie.</span><span class="sxs-lookup"><span data-stu-id="77d78-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="77d78-107">Un fichier de configuration de formulaire est un fichier avec l’extension .cfg et a un format similaire à un fichier d’initialisation de Windows.</span><span class="sxs-lookup"><span data-stu-id="77d78-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="77d78-108">Il est un fichier texte brut avec un nombre de sections.</span><span class="sxs-lookup"><span data-stu-id="77d78-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="77d78-109">Chaque section commence par un nom de section, placés entouré crochets.</span><span class="sxs-lookup"><span data-stu-id="77d78-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="77d78-110">Chaque section contient une ou plusieurs lignes qui définissent les valeurs et les paramètres relatifs à la section.</span><span class="sxs-lookup"><span data-stu-id="77d78-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="77d78-111">Valeurs de disposer d’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="77d78-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="77d78-112">Chaîne</span><span class="sxs-lookup"><span data-stu-id="77d78-112">String</span></span>
    
- <span data-ttu-id="77d78-113">Chaîne affichée</span><span class="sxs-lookup"><span data-stu-id="77d78-113">Displayed string</span></span>
    
- <span data-ttu-id="77d78-114">Chaîne de plateforme</span><span class="sxs-lookup"><span data-stu-id="77d78-114">Platform string</span></span>
    
- <span data-ttu-id="77d78-115">Nom de chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="77d78-115">Path name</span></span>
    
- <span data-ttu-id="77d78-116">Entier</span><span class="sxs-lookup"><span data-stu-id="77d78-116">Integer</span></span>
    
- <span data-ttu-id="77d78-117">GUID</span><span class="sxs-lookup"><span data-stu-id="77d78-117">GUID</span></span>
    
<span data-ttu-id="77d78-118">Pour plus d’informations sur les sections d’un fichier .cfg, voir [Fichier fichiers au Format de formulaire Configuration](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="77d78-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77d78-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77d78-119">See also</span></span>



[<span data-ttu-id="77d78-120">Développez serveurs de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="77d78-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

