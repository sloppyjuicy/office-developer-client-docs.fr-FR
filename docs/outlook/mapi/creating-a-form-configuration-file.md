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
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425217"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="a47a9-103">Création d’un fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="a47a9-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="a47a9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a47a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a47a9-105">Un fichier de configuration de formulaire fournit des informations sur un formulaire à la fois au gestionnaire de formulaires utilisé et aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="a47a9-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="a47a9-106">Un fichier de configuration de formulaire contient une spécification complète pour un formulaire, y compris les propriétés publiées par le formulaire pour une utilisation par les clients de messagerie, les verbes implémentés par le formulaire et les plateformes pris en charge par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a47a9-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="a47a9-107">Un fichier de configuration de formulaire est un fichier avec une extension .cfg et a un format similaire à celui d’un Windows d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="a47a9-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="a47a9-108">Il s’agit d’un fichier en texte simple avec un certain nombre de sections.</span><span class="sxs-lookup"><span data-stu-id="a47a9-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="a47a9-109">Chaque section commence par un nom de section, entre crochets.</span><span class="sxs-lookup"><span data-stu-id="a47a9-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="a47a9-110">Chaque section contient une ou plusieurs lignes qui définissent des valeurs et des paramètres pertinents pour cette section.</span><span class="sxs-lookup"><span data-stu-id="a47a9-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="a47a9-111">Les valeurs ont l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="a47a9-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="a47a9-112">String</span><span class="sxs-lookup"><span data-stu-id="a47a9-112">String</span></span>
    
- <span data-ttu-id="a47a9-113">Chaîne affichée</span><span class="sxs-lookup"><span data-stu-id="a47a9-113">Displayed string</span></span>
    
- <span data-ttu-id="a47a9-114">Chaîne de plateforme</span><span class="sxs-lookup"><span data-stu-id="a47a9-114">Platform string</span></span>
    
- <span data-ttu-id="a47a9-115">Nom de chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="a47a9-115">Path name</span></span>
    
- <span data-ttu-id="a47a9-116">Entier</span><span class="sxs-lookup"><span data-stu-id="a47a9-116">Integer</span></span>
    
- <span data-ttu-id="a47a9-117">GUID</span><span class="sxs-lookup"><span data-stu-id="a47a9-117">GUID</span></span>
    
<span data-ttu-id="a47a9-118">Pour plus d’informations sur les sections d’un fichier .cfg, voir Format de fichier des fichiers [de configuration de formulaire.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="a47a9-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a47a9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a47a9-119">See also</span></span>



[<span data-ttu-id="a47a9-120">Développement de serveurs de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="a47a9-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

