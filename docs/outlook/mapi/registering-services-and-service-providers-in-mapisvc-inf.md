---
title: Inscription de services et de fournisseurs de services dans MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Dernière modification : 18 juillet 2013'
ms.openlocfilehash: c74257b84636952b26c5a624f4f7f76f66be9149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566921"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Inscription de services et de fournisseurs de services dans MapiSvc.inf

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Installation d’un nouveau fournisseur sur un système nécessite la mise à jour du fichier MapiSvc.inf afin de pointer vers le nouveau fournisseur. Propriétés standard définie lors de la configuration, qui incluent les éléments suivants, informent MAPI où trouver la bibliothèque de liens dynamiques du fournisseur (.dll) :
  
- Le **PR_SERVICE_DLL_NAME** est spécifié dans la section **[Service Message]** . 
    
- Le **PR_PROVIDER_DLL_NAME** est spécifié dans la section **[Service Provider]** . 
    
> [!NOTE]
> Il est que vous définissez le nom du fichier .dll de votre fournisseur (sans le suffixe « 32 »). MAPI charge ensuite votre fournisseur en recherchant sur le chemin d’accès. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Le fait de placer un chemin d’accès dans le fichier MapiSvc.inf

La plupart des applications installer sous Program Files, nécessitant une mise à jour à la variable path pour permettre aux fournisseurs MAPI travailler. Avec quelques restrictions Microsoft Outlook 2010 et Outlook 2013 peuvent prendre en charge les chemins d’accès complets aux fournisseurs MAPI.
  
Lors de l’inscription de votre fournisseur dans MapiSvc.inf, vous pouvez placer le chemin d’accès complet au fournisseur dans les propriétés MAPI **PR_SERVICE_DLL_NAME** et **PR_PROVIDER_DLL_NAME**.
  
Dans des propriétés, le chemin d’accès complet doit être sans le suffixe « 32 », parce que MAPI continue qui ajouter au nom de fichier avant de rechercher le fichier. Cela signifie que si vous enregistrez le chemin d’accès « c:\mypath\myprovider.dll », MAPI tente de charger « c:\mypath\myprovider32.dll ».
  
Étant donné que Outlook MAPI n’a pas été conçu pour prendre en charge les chemins d’accès complets, elle effectue cette insertion du suffixe « 32 » en recherchant la première période dans la chaîne, ce qui signifie que les chemins d’accès qui contiennent des autres périodes ne fonctionnent pas, vous ne pouvez pas utiliser des chemins d’accès tel que « c:\my.path\myprovider.dll » ou « c:\mypath\my.provider.dll ».
  
Parfois dans un fournisseur de magasins, vous allez générer les identificateurs d’entrée à l’aide de la fonction **WrapStoreEntryID** , qui prend comme paramètre le nom de votre fournisseur. 
  
> [!IMPORTANT]
> Si vous utilisez des chemins d’accès complets dans MapiSvc.inf, vous devez utiliser le même chemin d’accès dans les appels à **WrapStoreEntryID**. 
  
En outre, le chemin d’accès que vous utilisez peut-être être converti vers et depuis Unicode à l’aide de la page de code fournie par la fonction [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) . 
  
> [!CAUTION]
> Vous pouvez rencontrer échec si vous choisissez un chemin d’accès contenant des caractères qui ne peuvent pas survivre tel un aller-retour via les fonctions [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) et [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) . 
  
Pour une démonstration de cette fonctionnalité, l' [exemple PST encapsulé](http://ol2010mapisamples.codeplex.com/) sur CodePlex a été modifiée : la fonctionnalité pertinente **MergeWithMapiSvc** et **GenerateProviderPath**.
  

