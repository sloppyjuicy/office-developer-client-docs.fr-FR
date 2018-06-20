---
title: Format de fichier des fichiers de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: def91b4e28e60f6d2e8534f0ed7261777ec0c8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783290"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="1ddfd-103">Format de fichier des fichiers de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="1ddfd-103">File format of form configuration files</span></span>

<span data-ttu-id="1ddfd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ddfd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ddfd-105">Un fichier de configuration de formulaire est un fichier de mise en forme créé par les développeurs de formulaires pour définir un formulaire.</span><span class="sxs-lookup"><span data-stu-id="1ddfd-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="1ddfd-106">Étant donné que les fichiers de configuration de formulaire sont utilisés par les responsables de formulaire pour charger des formulaires, chaque formulaire doit être défini à l’aide d’un fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="1ddfd-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="1ddfd-107">Fichiers de configuration de formulaire doivent avoir l’extension de nom de fichier .cfg.</span><span class="sxs-lookup"><span data-stu-id="1ddfd-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="1ddfd-108">Le fichier suit la syntaxe générale d’un fichier d’initialisation de Windows (fichier .ini).</span><span class="sxs-lookup"><span data-stu-id="1ddfd-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="1ddfd-109">Il est divisé en sections nommées, et chaque section contient une série d’entrées et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="1ddfd-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="1ddfd-110">Valeurs de doivent d’un des types suivants : chaîne, chaîne affichée, chaîne de plateforme, chemin d’accès, integer ou **GUID**, identificateur global unique.</span><span class="sxs-lookup"><span data-stu-id="1ddfd-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="1ddfd-111">Fichiers de configuration de formulaire peuvent être créés avec n’importe quel éditeur de texte ou le traitement de texte qui est capable d’enregistrer des fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="1ddfd-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

