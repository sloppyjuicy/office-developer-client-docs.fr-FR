---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331541"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="65976-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="65976-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="65976-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65976-105">Affiche une feuille de propriétés qui permet à l'utilisateur de modifier la configuration d'un fournisseur de services cette méthode n'est pas prise en charge dans les objets Status implémentés par MAPI.</span><span class="sxs-lookup"><span data-stu-id="65976-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="65976-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65976-106">Parameters</span></span>

 <span data-ttu-id="65976-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="65976-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="65976-108">dans Handle de la fenêtre parente de la feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="65976-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="65976-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="65976-109">_ulFlags_</span></span>
  
> <span data-ttu-id="65976-110">dans Masque de des indicateurs qui contrôle l'affichage de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="65976-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="65976-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="65976-111">The following flag can be set:</span></span>
    
<span data-ttu-id="65976-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="65976-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="65976-113">Indique que le fournisseur ne doit pas permettre aux utilisateurs de modifier les propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="65976-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="65976-114">Cet indicateur n'est qu'une suggestion; elle peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="65976-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65976-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65976-115">Return value</span></span>

<span data-ttu-id="65976-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="65976-116">S_OK</span></span> 
  
> <span data-ttu-id="65976-117">La feuille de propriétés de configuration a été correctement affichée.</span><span class="sxs-lookup"><span data-stu-id="65976-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="65976-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="65976-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="65976-119">L'objet Status ne prend pas en charge cette méthode, comme indiqué par l'absence de l'indicateur STATUS_SETTINGS_DIALOG dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="65976-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65976-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="65976-120">Remarks</span></span>

<span data-ttu-id="65976-121">La méthode **IMAPIStatus:: SettingsDialog** affiche une feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="65976-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="65976-122">Tous les fournisseurs de services doivent prendre en charge la méthode **SettingsDialog** , mais cela n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="65976-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="65976-123">Les fournisseurs de services peuvent implémenter leurs propres feuilles de propriétés ou utiliser l'implémentation fournie dans la méthode [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) de l'objet de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="65976-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="65976-124">**DoConfigPropsheet** génère une feuille de propriétés en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="65976-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="65976-125">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="65976-125">Notes to implementers</span></span>

<span data-ttu-id="65976-126">Si un fournisseur de transport distant possède des paramètres, il doit effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="65976-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="65976-127">Ouvrez la section Profil du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="65976-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="65976-128">Obtenir les paramètres de propriété du fournisseur de transport à partir du profil.</span><span class="sxs-lookup"><span data-stu-id="65976-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="65976-129">Affichez les paramètres de propriété dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="65976-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="65976-130">Si la boîte de dialogue permet de modifier les paramètres de propriété, vérifiez que les nouveaux paramètres sont valides et stockez-les à nouveau dans la section Profil du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="65976-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="65976-131">Renvoie S_OK ou toute valeur d'erreur renvoyée lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="65976-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="65976-132">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="65976-132">Notes to callers</span></span>

<span data-ttu-id="65976-133">Vous pouvez utiliser la feuille de propriétés affichée via **SettingsDialog** pour effectuer diverses tâches, telles que les suivantes:</span><span class="sxs-lookup"><span data-stu-id="65976-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="65976-134">Spécifiez une banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="65976-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="65976-135">Spécifiez un ordre de transport.</span><span class="sxs-lookup"><span data-stu-id="65976-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="65976-136">Spécifiez un conteneur de carnet d'adresses par défaut pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="65976-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="65976-137">Spécifiez un ordre de recherche pour résoudre les noms ambigus.</span><span class="sxs-lookup"><span data-stu-id="65976-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="65976-138">Spécifiez un carnet d'adresses personnel par défaut.</span><span class="sxs-lookup"><span data-stu-id="65976-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="65976-139">Les fournisseurs de services peuvent implémenter des feuilles de propriétés qui sont en lecture/écriture, en lecture seule ou une combinaison d'autorisations, en fonction de la propriété.</span><span class="sxs-lookup"><span data-stu-id="65976-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="65976-140">Les fournisseurs de services peuvent implémenter différentes autorisations sur les propriétés individuelles en définissant des restrictions de propriété.</span><span class="sxs-lookup"><span data-stu-id="65976-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="65976-141">Le mode par défaut des feuilles de propriétés est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="65976-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="65976-142">Vous pouvez demander des feuilles de propriétés en lecture seule en définissant l'indicateur UI_READONLY dans vos appels à **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="65976-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="65976-143">Les fournisseurs de services qui sont en mesure d'implémenter des feuilles de propriétés en lecture seule peuvent le faire.</span><span class="sxs-lookup"><span data-stu-id="65976-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="65976-144">Toutefois, étant donné que certains fournisseurs de services ne peuvent pas remplacer le mode par défaut, vous devez être prêt à gérer les feuilles de propriétés des deux types.</span><span class="sxs-lookup"><span data-stu-id="65976-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="65976-145">Étant donné qu'une interface utilisateur est toujours impliquée dans cette opération, seuls les clients interactifs doivent appeler **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="65976-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65976-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65976-146">See also</span></span>



[<span data-ttu-id="65976-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="65976-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="65976-148">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="65976-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="65976-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="65976-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

