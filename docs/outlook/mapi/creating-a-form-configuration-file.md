---
title: Création d’un fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8159d93aef020d7c9c1b56be4cf6256f80b8aa3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584166"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="b641e-103">Création d’un fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="b641e-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="b641e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b641e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b641e-105">Un fichier de configuration de formulaire fournit des informations sur un formulaire à la fois dans le Gestionnaire de formulaire utilisée et pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="b641e-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="b641e-106">Un fichier de configuration de formulaire contient une spécification d’étendue pour un formulaire, y compris les propriétés publiées par le formulaire pour une utilisation par les clients, les verbes implémentées par le formulaire et les plateformes prises en charge par le formulaire de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b641e-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="b641e-107">Un fichier de configuration de formulaire est un fichier avec l’extension .cfg et a un format similaire à un fichier d’initialisation de Windows.</span><span class="sxs-lookup"><span data-stu-id="b641e-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="b641e-108">Il est un fichier texte brut avec un nombre de sections.</span><span class="sxs-lookup"><span data-stu-id="b641e-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="b641e-109">Chaque section commence par un nom de section, placés entouré crochets.</span><span class="sxs-lookup"><span data-stu-id="b641e-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="b641e-110">Chaque section contient une ou plusieurs lignes qui définissent les valeurs et les paramètres relatifs à la section.</span><span class="sxs-lookup"><span data-stu-id="b641e-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="b641e-111">Valeurs de disposer d’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="b641e-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="b641e-112">String</span><span class="sxs-lookup"><span data-stu-id="b641e-112">String</span></span>
    
- <span data-ttu-id="b641e-113">Chaîne affichée</span><span class="sxs-lookup"><span data-stu-id="b641e-113">Displayed string</span></span>
    
- <span data-ttu-id="b641e-114">Chaîne de plateforme</span><span class="sxs-lookup"><span data-stu-id="b641e-114">Platform string</span></span>
    
- <span data-ttu-id="b641e-115">Nom de chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b641e-115">Path name</span></span>
    
- <span data-ttu-id="b641e-116">Entier</span><span class="sxs-lookup"><span data-stu-id="b641e-116">Integer</span></span>
    
- <span data-ttu-id="b641e-117">GUID</span><span class="sxs-lookup"><span data-stu-id="b641e-117">GUID</span></span>
    
<span data-ttu-id="b641e-118">Pour plus d’informations sur les sections d’un fichier .cfg, voir [Fichier fichiers au Format de formulaire Configuration](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="b641e-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b641e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b641e-119">See also</span></span>



[<span data-ttu-id="b641e-120">Développement de serveurs de formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="b641e-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

