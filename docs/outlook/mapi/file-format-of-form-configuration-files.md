---
title: Format des fichiers config des formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d07d88d7b8b892a82832f91989e322ea3b32e040
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415550"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="7acfc-103">Format des fichiers config des formulaires</span><span class="sxs-lookup"><span data-stu-id="7acfc-103">File format of form configuration files</span></span>

<span data-ttu-id="7acfc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7acfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7acfc-105">Un fichier de configuration de formulaire est un fichier mis en forme créé par les développeurs de formulaires pour définir un formulaire.</span><span class="sxs-lookup"><span data-stu-id="7acfc-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="7acfc-106">Étant donné que les fichiers de configuration de formulaire sont utilisés par les gestionnaires de formulaires pour charger des formulaires, chaque formulaire doit être défini à l'aide d'un fichier de configuration de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7acfc-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="7acfc-107">Les fichiers de configuration de formulaire doivent être dotés de l'extension de nom de fichier. cfg.</span><span class="sxs-lookup"><span data-stu-id="7acfc-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="7acfc-108">Le fichier suit la syntaxe générale d'un fichier d'initialisation Windows (fichier. ini).</span><span class="sxs-lookup"><span data-stu-id="7acfc-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="7acfc-109">Elle est divisée en sections nommées et chaque section contient une série d'entrées et de valeurs.</span><span class="sxs-lookup"><span data-stu-id="7acfc-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="7acfc-110">Les valeurs ont l'un des types suivants: String, chaîne affichée, chaîne de plateforme, chemin d'accès, entier ou identificateur global unique, **GUID**.</span><span class="sxs-lookup"><span data-stu-id="7acfc-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="7acfc-111">Les fichiers de configuration de formulaire peuvent être créés avec un éditeur de texte ou un traitement de texte capable d'enregistrer des fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="7acfc-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

