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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783964"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="f3b96-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="f3b96-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="f3b96-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3b96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3b96-105">Affiche une feuille de propriétés qui permet à l’utilisateur de modifier la configuration d’un fournisseur de services que cette méthode n’est pas pris en charge dans les objets état implémentés par MAPI.</span><span class="sxs-lookup"><span data-stu-id="f3b96-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f3b96-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3b96-106">Parameters</span></span>

 <span data-ttu-id="f3b96-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f3b96-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f3b96-108">[in] Un handle vers la fenêtre parent de la feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="f3b96-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="f3b96-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3b96-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f3b96-110">[in] Masque de bits d’indicateurs qui contrôle l’affichage de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f3b96-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="f3b96-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="f3b96-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f3b96-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="f3b96-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="f3b96-113">Indique que le fournisseur ne doit pas activer aux utilisateurs de modifier les propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="f3b96-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="f3b96-114">Cet indicateur n’est qu’une suggestion ; Il peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="f3b96-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3b96-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f3b96-115">Return value</span></span>

<span data-ttu-id="f3b96-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3b96-116">S_OK</span></span> 
  
> <span data-ttu-id="f3b96-117">La feuille de propriétés de configuration a été correctement affichée.</span><span class="sxs-lookup"><span data-stu-id="f3b96-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="f3b96-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f3b96-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f3b96-119">L’objet état ne gère pas cette méthode, comme indiqué par l’absence de l’indicateur STATUS_SETTINGS_DIALOG dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f3b96-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3b96-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3b96-120">Remarks</span></span>

<span data-ttu-id="f3b96-121">La méthode **IMAPIStatus::SettingsDialog** affiche une feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="f3b96-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="f3b96-122">Tous les fournisseurs de services doivent prendre en charge la méthode **dialogue** , mais il n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f3b96-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="f3b96-123">Fournisseurs de service peuvent implémenter leurs propres feuilles de propriétés ou utilisez l’implémentation fournie dans la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) de l’objet de la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f3b96-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="f3b96-124">**DoConfigPropsheet** génère une feuille de propriétés en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="f3b96-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f3b96-125">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f3b96-125">Notes to implementers</span></span>

<span data-ttu-id="f3b96-126">Si un fournisseur de transport à distance possède des paramètres, il doit procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f3b96-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="f3b96-127">Ouvrez la section de profil du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="f3b96-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="f3b96-128">Obtenez le transport paramètres du fournisseur de la propriété du profil.</span><span class="sxs-lookup"><span data-stu-id="f3b96-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="f3b96-129">Afficher les paramètres des propriétés dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f3b96-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="f3b96-130">Si la boîte de dialogue permet de modifier les paramètres de la propriété, vérifiez que les nouveaux paramètres sont valides et les stockent dans la section de profil du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="f3b96-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="f3b96-131">Renvoie S_OK, ou les valeurs d’erreur renvoyés au cours des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="f3b96-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="f3b96-132">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f3b96-132">Notes to callers</span></span>

<span data-ttu-id="f3b96-133">Vous pouvez utiliser la feuille des propriétés affichée par le biais de **dialogue** pour effectuer diverses tâches, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3b96-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="f3b96-134">Spécifiez une banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="f3b96-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="f3b96-135">Spécifier un ordre de transport.</span><span class="sxs-lookup"><span data-stu-id="f3b96-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="f3b96-136">Spécifier un conteneur de carnet d’adresses par défaut pour la navigation.</span><span class="sxs-lookup"><span data-stu-id="f3b96-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="f3b96-137">Spécifiez un ordre de recherche pour la résolution des noms ambigus.</span><span class="sxs-lookup"><span data-stu-id="f3b96-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="f3b96-138">Spécifiez un carnet d’adresses personnel par défaut.</span><span class="sxs-lookup"><span data-stu-id="f3b96-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="f3b96-139">Fournisseurs de services peuvent implémenter des feuilles de propriétés qui sont en lecture/écriture, en lecture seule, ou une combinaison des autorisations en fonction de la propriété.</span><span class="sxs-lookup"><span data-stu-id="f3b96-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="f3b96-140">Fournisseurs de services peuvent implémenter des autorisations différentes sur des propriétés individuelles en définissant les restrictions de propriété.</span><span class="sxs-lookup"><span data-stu-id="f3b96-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="f3b96-141">Le mode par défaut pour les feuilles de propriété est en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="f3b96-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="f3b96-142">Vous pouvez demander des feuilles de propriétés en lecture seule en définissant l’indicateur UI_READONLY dans vos appels à **dialogue**.</span><span class="sxs-lookup"><span data-stu-id="f3b96-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="f3b96-143">Fournisseurs de services qui sont en mesure d’implémenter des feuilles de propriétés en lecture seule peuvent le faire.</span><span class="sxs-lookup"><span data-stu-id="f3b96-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="f3b96-144">Étant donné que certains fournisseurs de services ne peuvent pas modifier le mode par défaut, vous devez être prêt à gérer les feuilles de propriétés de des types.</span><span class="sxs-lookup"><span data-stu-id="f3b96-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="f3b96-145">Car une interface utilisateur est toujours impliquée dans cette opération, seuls les clients interactives doivent appeler **dialogue**.</span><span class="sxs-lookup"><span data-stu-id="f3b96-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3b96-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3b96-146">See also</span></span>



[<span data-ttu-id="f3b96-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="f3b96-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="f3b96-148">Propriété canonique PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="f3b96-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="f3b96-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f3b96-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

